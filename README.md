<div align="center">
  <h1>Hi, I'm Matheus Dias 👋</h1>
  <p><strong>Systems, SRE & Platform Engineer | B.S. Electrical & Telecommunications Engineering</strong></p>
  <p>📍 São Paulo / Manaus, Brazil · 💼 Open to Remote Opportunities</p>

  <p>
    <a href="https://www.linkedin.com/in/matheusvdias/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
    <a href="https://matheusdiasportfolio.web.app/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Portfolio" /></a>
  </p>
</div>

<br/>

### ⚡ About Me
I bridge the gap between **low-level systems, distributed infrastructure, and high-performance client applications**. With a Bachelor's in **Electrical & Telecommunications Engineering** and 6+ years in software engineering, I design fault-tolerant systems, automate bare-metal Linux infrastructure, tune TCP network kernels, and architect resilient applications at scale.

- 🔭 **Currently Building:** Distributed bare-metal homelab infrastructure (OptiPlex + Raspberry Pi), high-concurrency Go backends, and network resilience packages.
- 🛠 **Engineering Focus:** Site Reliability Engineering (SRE), Linux Kernel Tuning (BBR, TCP buffer sizing), IaC, Containerization, and Observability.
- 🎓 **Academic Background:** B.S. in Electrical and Telecommunications Engineering (UniNorte) & Electronics Technician (IFAM).
- 📜 **Published Thesis:** *"IoT Data Center Environmental Telemetry & Real-Time Alert System on Raspberry Pi"*.

---

### 🛠 Tech Stack & Core Competencies

| Domain | Technologies |
| :--- | :--- |
| **Systems & Backend** | **Go (Golang)**, Linux (Debian, systemd, sysctl), Docker, REST/gRPC, WebSockets, SQL |
| **SRE & Infrastructure** | **Infrastructure-as-Code**, Kernel Tuning (BBR, swappiness), Cloudflare Zero Trust Tunnels, Tailscale, R2 Automated Backups, Prometheus, Grafana |
| **Client & Mobile Platform** | **Flutter**, **Dart**, **Native Android (Kotlin/Java)**, WASM, Offline-first sync architectures, Crashlytics (99.8%+ crash-free rate) |
| **Hardware & Telecom** | Distributed Homelabs, Telecommunications networks, Embedded Android POS terminals, IoT sensor pipelines |

---

### 🏗 Distributed Homelab Architecture (Production-at-Home)

```mermaid
graph TD
    subgraph WAN ["External Traffic (Internet)"]
        User["Clients & APIs"]
        CF["Cloudflare Edge (Zero Trust & DNS)"]
    end

    subgraph Homelab ["Bare-Metal Homelab Cluster"]
        direction TB
        subgraph Gateway ["Ingress & Security"]
            CFTunnel["cloudflared (Encrypted Zero Trust Tunnel)"]
        end

        subgraph Nodes ["Compute Nodes (Debian Linux - BBR Congestion Control)"]
            Dell["Dell OptiPlex Node<br/>• Immich Media Engine<br/>• PostgreSQL Engine<br/>• Go Liturgical Backend API"]
            RPI["Raspberry Pi 4 Node<br/>• Telemetry & Monitoring<br/>• Lightweight Edge Services"]
        end

        subgraph Storage ["Disaster Recovery & Backups"]
            LocalVol["Local NVMe / SSD Storage"]
            R2["Offsite Backup (Cloudflare R2 Bucket)"]
        end
    end

    User --> CF
    CF --> CFTunnel
    CFTunnel --> Dell
    CFTunnel --> RPI
    Dell --> LocalVol
    LocalVol -.->|Nightly Cron + Rclone| R2
```

---

### 🚀 Featured Engineering Repositories

* 🐧 **[homelab-infrastructure](https://github.com/Mathvdias/homelab-infrastructure)** — Infrastructure-as-Code for distributed bare-metal homelab running Linux (Debian), containerized microservices, kernel-level network optimizations (BBR, swappiness), and automated offsite backups to Cloudflare R2.
* ⚡ **[intercepted_http](https://github.com/Mathvdias/intercepted_http)** — A composable HTTP interceptor layer for `package:http`. Automatic OAuth2/JWT token refresh, exponential backoff retries, and observability telemetry with 100% test coverage.
* 🖥 **[portfolio](https://github.com/Mathvdias/portfolio)** — Desktop-inspired portfolio built with Flutter compiled to WebAssembly (WASM), featuring draggable window management, spotlight search, and comprehensive unit/widget tests.

---

<div align="center">
  <i>"In God we trust; all others must bring data." — W. Edwards Deming</i>
</div>
