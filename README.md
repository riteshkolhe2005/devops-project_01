# DevSecOps CI/CD Pipeline Using Jenkins, SonarQube & Trivy (Local Ubuntu)

This repository demonstrates a **complete DevSecOps CI/CD pipeline** built on a **single local Ubuntu VM** using **open-source tools only**.

The main goal of this project is to showcase:
- CI/CD automation
- Secure container builds
- Static code analysis
- Vulnerability scanning
- Docker-based deployment

> ⚠️ Disclaimer  
> The frontend and backend application code are used as a **sample workload**.  
> The application itself was **not developed by me**.  
> **All CI/CD design, Jenkins pipelines, Docker, security scanning, and deployment automation are implemented by me.**

---

## 🧱 System Architecture


### Overview
- All services run on **one Ubuntu VM**
- Jenkins, SonarQube, and PostgreSQL run as Docker containers
- Jenkins Agent connects via SSH
- Deployment happens on the same host using Docker Compose

---

## 🛠️ Technology Stack

| Category | Tools |
|--------|------|
| CI/CD | Jenkins |
| Code Quality | SonarQube |
| Security Scanning | Trivy |
| Containers | Docker, Docker Compose |
| Runtime | Node.js |
| OS | Ubuntu (Local VM) |

---

## 🔁 CI/CD Pipeline Flow


<img width="959" height="503" alt="image" src="https://github.com/user-attachments/assets/2b9804ef-8d06-45c3-a650-f28aedaa28ad" />

### Pipeline Stages
1. GitHub source checkout
2. Dependency installation
3. Static code analysis (SonarQube)
4. Docker image build
5. Vulnerability scanning (Trivy)
6. Push images to Docker Hub
7. Deploy application using Docker Compose

---

## ⚙️ Jenkins Configuration

### Jenkins Dashboard

<img width="688" height="494" alt="image" src="https://github.com/user-attachments/assets/6576ee37-bd64-4ac8-93b8-f203e73b9fb6" />

- Jenkins runs inside Docker
- SSH agent used for builds
- Credentials securely stored in Jenkins
- Tools managed via Jenkins Global Tool Configuration

---

## 🚀 Pipeline Execution Result


<img width="959" height="503" alt="image" src="https://github.com/user-attachments/assets/2b9804ef-8d06-45c3-a650-f28aedaa28ad" />


✔️ All pipeline stages executed successfully  
✔️ Security scans completed  
✔️ Deployment automated  

---

## 🧠 SonarQube Code Analysis

<img width="1919" height="1003" alt="image" src="https://github.com/user-attachments/assets/d97988c9-fae3-4fca-94c1-9b1a75bceaaf" />


- Static code analysis
- Detection of bugs, vulnerabilities, and code smells
- Quality metrics visible per project

---

## 🛡️ Trivy Vulnerability Scan



- Docker images scanned for vulnerabilities
- HIGH and CRITICAL severity checks
- Reports archived as Jenkins build artifacts

---

## 🐳 Docker Deployment Verification



- Frontend and backend containers running
- Jenkins, SonarQube, PostgreSQL containers active
- All services managed via Docker Compose

---

## 🌐 Application Access

### Frontend
<img width="700" height="392" alt="image" src="https://github.com/user-attachments/assets/7735195f-73b4-4693-ae3b-93b02a1b7aaf" />


Accessible at:
http://localhost:5173

yaml
Copy code

### Backend
<img width="638" height="377" alt="image" src="https://github.com/user-attachments/assets/93e32ecc-4d85-4238-ac91-e77c7cbbf659" />


Accessible at:
http://localhost:5000

yaml
Copy code

---

## 🔐 Security Practices Implemented

- No hard-coded secrets in repository
- Jenkins credentials used for:
  - Docker Hub authentication
  - SSH access
  - SonarQube token
- Trivy vulnerability scanning
- Jenkins containers hardened with:
  - Read-only filesystem
  - No privilege escalation
  - Temporary filesystem (tmpfs)

---

## 🎯 Key Learnings

- Designed and implemented a DevSecOps CI/CD pipeline
- Integrated security into CI/CD
- Automated Docker image lifecycle
- Used Jenkins agents via SSH
- Deployed applications using Docker Compose

---

## 📌 Future Enhancements

- Enforce SonarQube Quality Gates
- Add unit and integration testing stages
- Integrate Prometheus & Grafana
- Extend deployment to cloud platforms
- Kubernetes-based pipeline

---

## 👤 Author

**Ritesh Kolhe**  
Aspiring DevOps / Cloud Engineer  





