# Kubernetes 3-Tier Application (Helm)

This project demonstrates a full 3-tier application deployed on Kubernetes using Helm.

## 🏗 Architecture

* Frontend: Nginx (served via ConfigMap)
* Backend: Node.js API
* Database: MongoDB (StatefulSet)
* Reverse Proxy: Nginx (/api → backend)
* Deployment Tool: Helm

## 🚀 Features

* Helm templating for reusable deployments
* ConfigMap-based frontend customization
* Internal service communication via Kubernetes DNS
* Backend integration through reverse proxy
* Environment-based configuration (dev/prod ready)

## 📦 Deploy

```bash
helm install my-app ./my-3tier-app -n dev --create-namespace
```

## 🔍 Access

```bash
kubectl port-forward svc/frontend 8084:80 -n dev
```

Then open:

http://localhost:8084

## 📚 Learning Highlights

* Debugging Kubernetes networking issues
* ConfigMap + volume mounting
* Helm chart structuring
* Nginx reverse proxy configuration
* Service-to-service communication

---

## 🔄 Next Version

This project will be rebuilt using PostgreSQL for deeper database integration.
