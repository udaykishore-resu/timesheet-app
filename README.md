# Timesheet Application (React + Golang)

A full-stack Timesheet Management Application built with ReactJS (frontend) and Golang (backend).
The project is containerized using Docker, orchestrated using Kubernetes, and supports deployment via Helm charts.

This repository is designed to demonstrate a complete modern DevOps-ready architecture including local development, containerization, and Kubernetes deployment.

## 📌 Project Structure
```bash
.
├── docker-compose.yaml        # Local multi-container setup
├── helm-chart/                # Helm chart for Kubernetes deployment
├── k8s-manifests/             # Raw Kubernetes YAML manifests
├── README.md                  # Project documentation
├── timesheet-app-be/          # Backend service (Golang)
└── timesheet-app-fe/          # Frontend service (ReactJS)
```

## 🚀 Tech Stack
### Frontend (timesheet-app-fe)
- ReactJS
- TypeScript / JavaScript
- npm

### Backend (timesheet-app-be)
- Golang
- REST API

### DevOps / Deployment
- Docker
- Docker Compose
- Kubernetes
- Helm

## 🏗️ Application Architecture
- Frontend (React) runs as a web UI and communicates with backend APIs.
- Backend (Go) provides REST endpoints for timesheet operations.
- Both services can be deployed locally using Docker Compose or on Kubernetes using Helm / manifests.

## ⚙️ Local Development Setup
### 1️⃣ Clone the repository
```bash
git clone <your-repo-url>
cd <repo-folder>
```

## ▶️ Run Backend (Golang)
```bash
cd timesheet-app-be
go run main.go
```

Backend will start on a configured port (example: http://localhost:8080).

## ▶️ Run Frontend (React)
```bash
cd timesheet-app-fe
npm install
npm run dev
```

Frontend will start on a configured port (example: http://localhost:5173).

## 🐳 Run Full Application using Docker Compose

From root directory:

```bash
docker-compose up --build
```

To stop:
```bash
docker-compose down
```

This will start:

React Frontend container

Golang Backend container

## ☸️ Kubernetes Deployment (Raw Manifests)
### Apply Kubernetes YAML manifests
```bash
kubectl apply -f k8s-manifests/
```

### Verify deployments
```bash
kubectl get pods
kubectl get svc
```

To delete:
```bash
kubectl delete -f k8s-manifests/
```
## ⎈ Helm Deployment
### Deploy using Helm chart
```bash
helm install timesheet-app ./helm-chart
```

### Upgrade deployment
```bash
helm upgrade timesheet-app ./helm-chart
```

### Uninstall
```bash
helm uninstall timesheet-app
```

## 📌 Features (Planned / Supported)
- User login/authentication (optional enhancement)
- Create and manage timesheets
- Track working hours per day/week
- Submit timesheet entries
- Admin approval workflow (optional enhancement)
- Dashboard UI for timesheet overview

## 🔍 Useful Commands
### Docker
```bash
docker ps
docker images
docker logs <container_id>
```
### Kubernetes
```bash
kubectl get all
kubectl describe pod <pod-name>
kubectl logs <pod-name>
```

### Helm
```bash
helm list
helm status timesheet-app
```

## 📌 Notes
- Git does not track empty folders, so each folder contains at least one file.
- Kubernetes manifests are available in k8s-manifests/.
- Helm templates and values are available in helm-chart/.