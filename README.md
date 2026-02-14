# Smart ISP — Enterprise ISP Management Platform

An integrated solution for managing and operating an ISP network for residential complexes or large companies (2500+ users) using Docker on Windows with Hyper-V and WSL2, featuring advanced AI (Llama/GPT OSS 20B) for control, monitoring, automation, and smart technical support.

## 🚀 Key Features

- **Infrastructure & Networking:** Docker-based stack with OpenWrt, MikroTik CHR, Pi-hole, and Tailscale VPN.
- **AI Integration:** Integrated Llama.cpp GPU service for network monitoring, user behavior analysis, and smart support.
- **Full-Stack Backend:** Node.js Express API with JWT auth, MikroTik API integration, and Redis caching.
- **Robust Database:** MySQL 8.0 with Master/Slave replication for high availability.
- **Enterprise Monitoring:** Full observability stack with Prometheus, Grafana, and Alertmanager.
- **Egyptian Payment Gateways:** Built-in support for Vodafone Cash, Orange Money, Fawry, and eWallets.

## 🏗️ Project Structure

```text
smart-isp-platform/
├── backend/                # Node.js API Service
├── db/                     # Database schemas and init scripts
├── monitoring/             # Prometheus & Grafana configurations
├── nginx/                  # Reverse proxy & SSL configs
├── backup/                 # Automatic backup service
├── scripts/                # Utility scripts (health checks, etc.)
└── docker-compose.prod.yml # Production orchestration
```

## 🛠️ Quick Start

1. **Clone the repository:**
   ```bash
   git clone https://github.com/cookset/smart-isp-platform.git
   cd smart-isp-platform
   ```

2. **Environment Setup:** Create a `.env` file based on the provided configuration.

3. **Deploy with Docker Compose:**
   ```bash
   docker-compose -f docker-compose.prod.yml up -d --build
   ```

4. **Health Check:**
   ```powershell
   powershell ./scripts/health-check.ps1
   ```

## 🔒 Security & Privacy

- Isolated networks for Customers, Backend, and VPN.
- SSL/TLS encryption via Nginx.
- Secure management access via Tailscale VPN.
- Full audit logs for all administrative activities.

## 📄 License

This project is licensed under the MIT License.
