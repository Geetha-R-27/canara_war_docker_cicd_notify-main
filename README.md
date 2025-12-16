# Dockerizing a Maven webapp

This project implements a complete CI/CD pipeline for deploying a Java web application using GitHub, Jenkins, Maven, Docker, Tomcat, and AWS EC2. The pipeline supports Dev and Prod environments through Jenkins parameters, enabling automated builds, containerization, and environment-specific deployments. Dev uses Docker Compose for testing, while Prod pulls the latest Docker image, removes old containers, and runs a fresh instance. Cleanup automation is included to remove old containers and images. Designed & Developed by Sak_Shetty under MIT License.

## Prerequisites
- Docker installed
- Maven (for local builds) or use multi-stage Docker build
- JDK version matching your app (example uses JDK 11)
---

### ⚙️ Jenkins Parameters
| Param | Description |
|------|------------|
| ENVIRONMENT | dev / prod |
| ACTION | build / deploy |
| RECIPIENT_EMAIL | Email to receive alerts |
---

### 📨 Notification Environment Variables (Jenkins Credentials)
| Key | Description |
|----|-------------|
| GMAIL_USER | Gmail sender ID |
| GMAIL_APP_PASS | Gmail App Password |
---

### 🛠 Run Notification Script Manually (test)
```bash
GMAIL_USER="your@gmail.com" \
GMAIL_APP_PASS="xxxx" \
./jenkins_notify.sh SUCCESS sample-job 10 user@example.com
```
## Add Jenkins credential for DockerHub:
## Add Jenkins credential for Gmail:
- **Kind**: Username with password
- **Username**: your Gmail address
- **Password**: Gmail App Password
- **ID**: GMAIL_GMAILAUTH
---
## Project Photos
<img width="1741" height="933" alt="Screenshot 2025-12-16 181544" src="https://github.com/user-attachments/assets/5ff7935e-0a08-4336-b5d1-a3d8cf98c350" />

<img width="1907" height="890" alt="Screenshot 2025-12-16 180702" src="https://github.com/user-attachments/assets/921f0109-ffbb-4e14-aa2b-5f8586e6354e" />

<img width="1559" height="847" alt="Screenshot 2025-12-16 181112" src="https://github.com/user-attachments/assets/e5f130e6-67a2-4a40-bd94-d328132d9d79" />

<img width="730" height="390" alt="Screenshot 2025-12-16 180759" src="https://github.com/user-attachments/assets/eea7ae4e-ed95-450f-b8a8-e8369da76eb7" />


---
## GitHub Badges Block
<p align="center">
  <img src="https://img.shields.io/badge/Build-Passing-brightgreen?style=for-the-badge">
  <img src="https://img.shields.io/badge/Jenkins-CI%2FCD-blue?style=for-the-badge&logo=jenkins">
  <img src="https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white">
  <img src="https://img.shields.io/badge/Email%20Alerts-Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white">
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge">
  <img src="https://img.shields.io/badge/Author-sak__shetty-purple?style=for-the-badge&logo=github">
</p>
<p align="center">
  💡 Project crafted with passion by <b>whitehorse</b> 🚀
</p>
---

**Script Done By whitehorse**
