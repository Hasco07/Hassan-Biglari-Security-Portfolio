# Boundary Diagram (Mermaid)

Mermaid renders directly on GitHub. This diagram is **fictional** and shows boundary clarity (what is in/out).

```mermaid
flowchart LR
  classDef blocked fill:#f7d7d7,stroke:#b55,stroke-width:1px,color:#000;

  subgraph LAN["Kitsune LAN (Air‑Gapped / Offline)"]
    direction LR

    subgraph UZ["User Zone"]
      DevWS["Developer Workstations"]
    end

    subgraph AZ["Admin Zone"]
      AdminWS["Admin Workstations"]
    end

    subgraph SZ["Server Zone"]
      IdP["Directory Services / IdP"]
      Git["Source Control Server"]
      CI["Build / CI Server"]
      Art["Artifact Repository"]
      Test["Test Harness / Simulator"]
    end

    subgraph ST["Security Tooling"]
      SIEM["Central Logging / SIEM"]
      Scanner["Vulnerability Scanner"]
    end

    DevWS -->|Authenticate| IdP
    AdminWS -->|Privileged auth| IdP

    DevWS -->|Commit / Fetch| Git
    CI -->|Fetch source| Git
    CI -->|Store build outputs| Art
    CI -->|Execute tests| Test

    Git -->|Forward logs| SIEM
    CI -->|Forward logs| SIEM
    Art -->|Forward logs| SIEM
    Test -->|Forward logs| SIEM
    IdP -->|Auth/audit logs| SIEM

    Scanner -->|Scan (scheduled)| DevWS
    Scanner -->|Scan (scheduled)| Git
    Scanner -->|Scan (scheduled)| CI
    Scanner -->|Scan (scheduled)| Art
    Scanner -->|Scan (scheduled)| Test
  end

  Media["Controlled Media Transfer Point (Fictional)"]
  Ext["External Networks / Internet"]:::blocked

  Media -. "Approved import/export only" .-> LAN
  LAN -. "No direct connectivity" .-> Ext
