# 🛡️ Cybersecurity Home Lab & Systems Administration Portfolio
A collection of live projects focused on infrastructure deployment, secure remote access, and enterprise-grade security monitoring.

---

## 🏗️ Project 1: Enterprise SIEM/XDR Deployment (Wazuh)
**Status:** 🟡 In Progress (Dashboard Live)

**The Pitch:** "Deploying a centralized security monitoring solution to achieve full visibility into system logs and threat detection."

* **Tech Stack:** Ubuntu 24.04 LTS, Wazuh Manager, Java (JVM), File Integrity Monitoring (FIM).
* **Key Achievement:** Successfully provisioned the Wazuh Central Manager.
* **Troubleshooting & AI Collaboration:** * **The Challenge:** Encountered service failures during the initial Indexer boot-up due to default memory constraints.
    * **The AI Solution:** Collaborated with **Gemini** and **Grok** to interpret Java stack traces and optimize the JVM heap size for a virtualized environment.
* **Next Steps:** Deploying Wazuh Agents to Windows 11 endpoints and simulating attacks via Kali Linux.

---

## ☁️ Project 2: Secure Private Cloud (Nextcloud)
**Status:** 🟢 Completed

**The Pitch:** "A self-hosted, hardened productivity suite replacing third-party SaaS with a focus on data sovereignty."

* **Tech Stack:** Ubuntu, MariaDB, Apache, Tailscale (Mesh VPN).
* **Security Angle:** Zero-exposure configuration. The server is not reachable via the public internet; access is restricted to a private Tailscale WireGuard tunnel.
* **Troubleshooting:** Resolved "Untrusted Domain" errors by manually editing `config.php` to recognize Tailscale DNS hostnames.

---

## 🖥️ Project 3: Private Remote Support Relay (RustDesk)
**Status:** 🟢 Completed

**The Pitch:** "Implementation of a self-hosted remote desktop solution to facilitate secure cross-platform troubleshooting."

* **Tech Stack:** RustDesk Server (hbbs/hbbr), Ubuntu VM, Tailscale.
* **Why it matters:** Eliminates reliance on third-party relays, ensuring all session metadata and traffic remain within a privately controlled environment.
* **Skills Demonstrated:** Linux service management, firewall configuration (UFW), and network tunneling.

---

## 🤖 Methodology: The "AI-Augmented" Engineer
I leverage **Generative AI (Gemini/Grok)** as a force multiplier in my workflow. 
* **Rapid Prototyping:** Using LLMs to generate baseline configuration files and Bash scripts.
* **Log Analysis:** Utilizing AI to parse complex system logs for faster Root Cause Analysis (RCA).
* **Continuous Learning:** Engaging with AI to deep-dive into the "why" behind networking protocols and security vulnerabilities.

---

## 🛠️ Skills & Certifications
* **Certifications:** CompTIA A+, Network+, Security+
* **Education:** Cybersecurity Student at Columbus State University
* **Background:** Former Welder transitioning into Systems Administration.

### 💡 Why This Matters:
This project demonstrates my ability to integrate **Generative AI** into the DevOps workflow, using it to solve complex configuration issues and reduce "time-to-solution" while maintaining a deep understanding of the underlying systems.
