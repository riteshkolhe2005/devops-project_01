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

![Architecture](docs/architecture.png)

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

![Pipeline Flow](docs/pipeline-flow.png)

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
![Jenkins Dashboard](docs/jenkins-dashboard.png)

- Jenkins runs inside Docker
- SSH agent used for builds
- Credentials securely stored in Jenkins
- Tools managed via Jenkins Global Tool Configuration

---

## 🚀 Pipeline Execution Result

![Pipeline Success](docs/pipeline-success.png)

✔️ All pipeline stages executed successfully  
✔️ Security scans completed  
✔️ Deployment automated  

---

## 🧠 SonarQube Code Analysis

![SonarQube Report](docs/sonarqube-report.png)

- Static code analysis
- Detection of bugs, vulnerabilities, and code smells
- Quality metrics visible per project

---

## 🛡️ Trivy Vulnerability Scan

![Trivy Report](docs/trivy-report.png)

- Docker images scanned for vulnerabilities
- HIGH and CRITICAL severity checks
- Reports archived as Jenkins build artifacts

---

## 🐳 Docker Deployment Verification

![Docker Containers](docs/docker-containers.png)

- Frontend and backend containers running
- Jenkins, SonarQube, PostgreSQL containers active
- All services managed via Docker Compose

---

## 🌐 Application Access

### Frontend
![Frontend](docs/app-frontend.png)

Accessible at:
http://localhost:5173

yaml
Copy code

### Backend
![Backend](https://camo.githubusercontent.com/cc28bc75a1f908900895ce110aa5ad31e0b3b8c9e1280c5f86f42afc2233703c/68747470733a2f2f6d69726f2e6d656469756d2e636f6d2f76322f726573697a653a6669743a3633382f312a4a314270674f366c6a476d6a4a774849464f67704f512e706e67)

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


