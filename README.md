#🐧 Linux Labs — System Administration & Home Lab Services

🧠 A collection of Linux-based labs showcasing system administration, service deployment, and security operations using Docker and self-hosted tools in a home lab environment.

🧰 Tools & Platforms

🐧 Linux Distributions: Ubuntu Server 22.04 LTS, Debian 12

🐳 Containerization: Docker & Docker Compose

🛡️ Security / Monitoring: Wazuh SIEM, Pi-hole, Fail2Ban

📹 NVR & Surveillance: Frigate / ZoneMinder

🧠 Core Services: DNS Sinkhole, Syslog Collection, Reverse Proxy (Traefik / Nginx)

🧭 Learning Objectives

🖥️ Linux Server setup, user management, and security hardening

📦 Deploying and managing containerized services with Docker

🧱 Building a modular home lab that simulates enterprise infrastructure

🌐 DNS filtering and security logging for internal networks

🧠 Centralized monitoring using Wazuh SIEM and syslog ingestion

📂 Lab Index
Lab Name	Description	Technologies Used	Link
🧭 Base Server Setup	Install & secure Linux for service hosting	Ubuntu Server, SSH, UFW	View

🐳 Docker Engine & Compose	Install Docker and deploy test containers	Docker, Portainer, Linux	View

🧠 Wazuh SIEM Deployment	Deploy Wazuh for log collection & analysis	Docker Compose, Wazuh, Syslog	View

🕳️ Pi-hole DNS Sinkhole	Block ads and malicious domains on LAN	Docker, Pi-hole, DNS	View

📹 NVR & Surveillance	Self-hosted NVR system for cameras	Frigate / ZoneMinder, Docker	View

🔗 Each lab folder contains its own README.md with step-by-step setup, architecture diagrams, and key takeaways.

🧪 Highlight: Wazuh SIEM Deployment
<details> <summary>📜 <strong>Click to expand</strong></summary>
🧠 Goal

Deploy a Wazuh SIEM stack to collect and analyze logs from multiple hosts in the home lab.

📦 Components

Wazuh Manager

Wazuh Indexer

Wazuh Dashboard

Syslog forwarders on Linux hosts

⚙️ Deployment
git clone https://github.com/wazuh/wazuh-docker.git
cd wazuh-docker
docker-compose -f generate-indexer-certs.yml run --rm generator
docker-compose up -d


Access the Wazuh dashboard at:
👉 https://localhost:5601

</details>
🧭 Roadmap

 Deploy reverse proxy (Traefik) for service routing

 Add centralized syslog collection using Rsyslog or Fluentd

 Integrate OpenVAS for vulnerability scanning

 Add monitoring with Grafana + Prometheus stack

 Automate backups & disaster recovery testing

📝 Disclaimer

⚠️ These labs are for educational and personal use in a controlled home lab environment.
They are not production deployments and should be secured appropriately before being exposed externally.
