# Hi, I'm Cole Suk 👋

Aspiring DevOps Engineer building real infrastructure in a home lab.

## 🛠️ What I work with

**Languages**
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat&logo=php&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat&logo=gnu-bash&logoColor=white)
![HTML](https://img.shields.io/badge/HTML-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-663399?style=flat&logo=css&logoColor=white)
![Lua](https://img.shields.io/badge/Lua-2C2D72?style=flat&logo=lua&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white)

**Infrastructure & DevOps**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=flat&logo=proxmox&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![Arch Linux](https://img.shields.io/badge/Arch_Linux-1793D1?style=flat&logo=arch-linux&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat&logo=ansible&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Gitea](https://img.shields.io/badge/Gitea-609926?style=flat&logo=gitea&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white)

**Networking & Observability**
![Tailscale](https://img.shields.io/badge/Tailscale-242424?style=flat&logo=tailscale&logoColor=white)
![Caddy](https://img.shields.io/badge/Caddy-1F88C0?style=flat&logo=caddy&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat&logo=nginx&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat&logo=mariadb&logoColor=white)

## 🌱 Currently learning / building

- **Monitoring & logging** — Prometheus, Alertmanager, and Grafana are running; now building out Loki with Grafana Alloy for centralized logs, and learning PromQL
- **Docker & Kubernetes** — fundamentals done; running most homelab services with Docker Compose, with Kubernetes practice on k3d locally (Deployments, Services, Ingress, ConfigMaps/Secrets, persistent storage)
- **Ansible** — key-based SSH and an inventory covering the homelab hosts; working toward playbooks for deploying services and scripts
- **Networking** — VLAN segmentation (Management / Homelab / Trusted), zone-based firewalls, DNS, routing, and remote access via a Tailscale subnet router
- **SQL** — joins, subqueries, aggregation, and relational database design
- **Linux systems administration** — process management, systemd, scripting, and firewalls (nftables), working through the *UNIX and Linux System Administration Handbook*
- **Next up:** AWS, Terraform/OpenTofu, and CI/CD pipelines with Gitea Actions / GitHub Actions

## 🏠 Home Lab

A self-hosted lab on Proxmox (Ryzen 7 5700X, RTX 4070 Ti Super for local AI), with each service isolated in its own LXC container or VM:

- **Storage** — OpenMediaVault NAS on mirrored 4TB drives, serving SMB shares and acting as the backup target for other services
- **DNS** — clustered Technitium DNS (primary + secondary) running an internal `home.lab` zone with reverse lookups
- **HTTPS** — Caddy reverse proxy with its own internal CA, putting every service behind HTTPS on `*.home.lab`
- **Remote access** — always-on Tailscale subnet router for secure access to the whole lab from anywhere
- **Git** — self-hosted Gitea
- **Web stack** — nginx, PHP-FPM, and MariaDB in Docker Compose, hosting a self-built dashboard for my lab services
- **Notes** — Trilium sync server with nightly backups to the NAS via systemd timers and rsync
- **Monitoring** — Prometheus, node_exporter on every host, Grafana dashboards, and Alertmanager; Loki for logs in progress
- **Notifications** — Postfix relay through Proton Bridge for email, plus ntfy for push alerts from scripts and monitoring
- **Automation** — dedicated Python scripts host running scheduled jobs as systemd services in isolated venvs
- **Local AI** — Hermes Agent in a VM with GPU passthrough, running local LLMs through Ollama with self-hosted SearXNG for private web search, as a day-to-day sysadmin assistant
