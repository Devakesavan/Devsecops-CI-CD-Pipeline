# 🚀 Full DevSecOps CI/CD Pipeline — Jenkins | SonarQube | OWASP | Trivy | Docker | Kubernetes | AWS EKS | Prometheus | Grafana

This project implements a complete automated DevSecOps CI/CD pipeline that takes source code from GitHub, performs quality and security checks, builds a Docker image, deploys it to Amazon EKS, and continuously monitors the running application using Prometheus & Grafana. The application used for deployment is a Hotstar Replica UI.

---

## 📌 Architecture Workflow

```
GitHub → Jenkins → SonarQube → OWASP FS Scan → Trivy FS Scan → Docker Build & Push → Trivy Image Scan → Kubernetes Deployment → AWS EKS → AWS Load Balancer → Prometheus + Grafana → Final Application
```

---

## 🧰 Tools & Technologies Used

| Category | Tools |
|---------|-------|
| Version Control | Git & GitHub |
| CI/CD | Jenkins |
| Code Quality | SonarQube |
| Security | OWASP Scan, Trivy FS Scan, Trivy Image Scan |
| Containerization | Docker & Docker Hub |
| Infrastructure | Kubernetes, Amazon EKS, Terraform |
| Monitoring | Prometheus, Grafana, Blackbox Exporter |
| Notifications | Gmail Pipeline Email |

---

## 🔥 Key Features

- Fully automated DevSecOps CI/CD pipeline
- Code quality validation using SonarQube Quality Gate
- Dual-layer filesystem vulnerability scanning using OWASP + Trivy
- Container image scanning using Trivy (NVD database)
- Docker image versioning and storage in Docker Hub
- Zero-downtime deployment to AWS EKS via rolling updates
- External endpoint monitoring using Blackbox Exporter
- Real-time Grafana dashboards with alerting
- Email notification with scan reports after deployment

---

## 🧩 Pipeline Stages

1. Code commit triggers Jenkins pipeline
2. SonarQube static code analysis and quality gate validation
3. OWASP and Trivy filesystem scans
4. Docker image build and push to Docker Hub
5. Trivy image scan validation
6. Kubernetes deployment using `kubectl apply`
7. AWS Load Balancer exposes the application publicly
8. Continuous monitoring using Prometheus, Grafana & Blackbox Exporter

---

## 📸 Screenshots

- Architecture Workflow Diagram  
- Jenkins Pipeline Stage View  
- SonarQube Dashboard  
- OWASP / Trivy Filesystem Scan  
- Docker Hub Repository  
- Trivy Image Scan  
- CI/CD Email Notification  
- Kubernetes Deployment  
- AWS EKS Cluster  
- AWS Load Balancer  
- Prometheus Targets / Blackbox Exporter  
- Grafana Dashboards  
- Final Application (Hotstar Replica)

Screenshots are available in the `/screenshots` folder.

---

## 🏗 Project Structure

```
.
├── k8s-manifests/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml (optional)
├── Jenkinsfile
├── Dockerfile
├── sonar-project.properties
└── src/
```

---

## ▶ Local Development

```bash
git clone <repository-url>
cd <project-folder>
npm install
npm start
```

---

## 📦 Build Docker Image Manually (Optional)

```bash
docker build -t <dockerhub-username>/<image-name>:v1 .
docker push <dockerhub-username>/<image-name>:v1
```

---

## ☸ Deploy to Kubernetes Manually (Optional)

```bash
kubectl apply -f k8s-manifests/
kubectl get pods
kubectl get svc
```

---

## 📡 Monitoring Access

| Component | URL |
|----------|-----|
| Prometheus | http://<monitoring-ip>:9090 |
| Grafana | http://<monitoring-ip>:3000 |
| Blackbox Exporter | http://<monitoring-ip>:9115 |

---

## 🌟 Final Output

A production-ready Hotstar-style web application running on AWS EKS and updated automatically through CI/CD and DevSecOps automation.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss the proposal.

---

## 📬 Contact

- LinkedIn: <your link>
- Email: <your email>

---

## ⭐ Support

If you found this project useful, please consider starring the repository. It encourages more DevOps open-source projects.
