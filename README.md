# Home-Lab-Secure-Services-And-Continuous-Learning
This is a project portfolio for the home lab I have been building and working on.


# Secure Home Lab: Private Cloud & Remote Access
A documented implementation of a self-hosted infrastructure focusing on data sovereignty and secure remote administration.

## 🛠️ Tech Stack
* **OS:** Ubuntu 24.04 LTS (Virtual Machines)
* **Networking:** Tailscale (WireGuard-based Mesh VPN)
* **Services:** Nextcloud (Private Cloud), RustDesk (Remote Desktop)
* **Database:** MariaDB

---

## ☁️ Project 1: Nextcloud Deployment
**Objective:** Replace third-party SaaS providers with a self-hosted, encrypted productivity suite.

### 🛡️ Security Implementation
* **Zero-Trust Access:** Configured the server to listen only on the Tailscale interface. No public ports (80/443) were opened on the router, preventing external brute-force attempts.
* **Hardened Database:** Implemented a dedicated MariaDB instance with restricted user permissions.

### 🚧 Challenge & Solution
* **Challenge:** Facing "Access through untrusted domain" errors when connecting via Tailscale.
* **Solution:** Modified the `config.php` file to include the Tailscale IP and DNS name in the `trusted_domains` array, ensuring the application recognized the secure VPN tunnel.

---

## 🖥️ Project 2: Self-Hosted RustDesk Relay
**Objective:** Establish a private remote support environment to manage home lab nodes without relying on public relay servers.

### 🛡️ Security Implementation
* **Private Signaling:** Hosted the `hbbs` and `hbbr` services internally, ensuring all remote session metadata stays within my controlled environment.
* **Encrypted Tunnels:** Used Tailscale to bridge the connection between my laptop and the VM, ensuring end-to-end encryption.

### 🚧 Challenge & Solution
* **Challenge:** Intermittent connection timeouts during initial setup.
* **Solution:** Identified that the UFW (Uncomplicated Firewall) on Ubuntu was blocking the specific heartbeat ports. Created a custom UFW rule to allow traffic on ports 21115-21119.

---

* ## 🤖 Development Methodology: AI-Augmented Troubleshooting
To accelerate deployment and ensure security best practices, I utilized **Gemini** and **Grok** as virtual engineering partners.

### 🛠️ How AI Was Leveraged:
* **Architecture Validation:** Consulted AI to verify the security of using Tailscale as an overlay network versus traditional port forwarding.
* **Rapid Troubleshooting:** Used LLMs to interpret Linux log files (`/var/log/syslog`) and identify specific database permission errors during the Nextcloud setup.
* **Documentation & Refinement:** Leveraged AI to structure technical documentation and refine Bash scripts for deployment efficiency.

### 💡 Why This Matters:
This project demonstrates my ability to integrate **Generative AI** into the DevOps workflow, using it to solve complex configuration issues and reduce "time-to-solution" while maintaining a deep understanding of the underlying systems.
