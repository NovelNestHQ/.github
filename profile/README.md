# 📚 NovelNest – A Community-Powered Books Marketplace

Welcome to the official GitHub Organization of **NovelNest**, a microservices-based platform for book lovers to **discover**, **buy**, **sell**, and **manage** physical books.  

This platform demonstrates scalable service engineering using modern web development, containerization, and orchestration technologies.



## 🧱 Architecture at a Glance

NovelNest is built using a modular, microservices-based architecture. Each service is maintained in its own repository and communicates via both synchronous REST APIs and asynchronous message queues using RabbitMQ.

### 🔧 Core Services

| Service         | Responsibilities                                                  | Tech Stack                       |
|----------------|--------------------------------------------------------------------|----------------------------------|
| User Service    | Authentication (SuperTokens), user profile & purchase history     | Node.js, TypeScript, PostgreSQL  |
| Catalog Service | Book catalog browsing & search (read-optimized)                   | Node.js, TypeScript, MongoDB     |
| Inventory Service | Manage book listings & stock (write-optimized)                 | Node.js, TypeScript, PostgreSQL  |
| Order Service   | Order lifecycle management, seller-buyer coordination             | Node.js, TypeScript, PostgreSQL  |
| Frontend UI     | React-based SPA interfacing with Kong API Gateway                 | React, TypeScript, NGINX         |

### 🌐 Infrastructure

- **Kong API Gateway**: Manages routing, security, and service exposure  
- **RabbitMQ**: Enables asynchronous inter-service communication  
- **Kubernetes (Minikube)**: Manages container orchestration and deployments  
- **Quay.io**: Hosts Docker container images for all services  

---

## 📂 GitHub Repositories

| Component          | Repository Link                                                                 |
|--------------------|----------------------------------------------------------------------------------|
| User Service        | [user-service](https://github.com/NovelNestHQ/user-service)                     |
| Catalog Service     | [catalog-service](https://github.com/NovelNestHQ/catalog-service)               |
| Inventory Service   | [inventory-service](https://github.com/NovelNestHQ/inventory-service)           |
| Order Service       | [order-service](https://github.com/NovelNestHQ/order-service)                   |
| Frontend UI         | [frontend](https://github.com/NovelNestHQ/frontend)                             |
| Kubernetes Manifests| [k8s-manifests](https://github.com/NovelNestHQ/k8s-manifests)                   |

---

## 📜 Documentation & Demonstrations

- 📘 **[Technical Documentation (PDF)](https://drive.google.com/file/d/1Vxrej8pZAZvGbFhOCBFYtVUE-BPhsiUa/view?usp=drive_link)**  
- 🎥 **Walkthrough Videos**:
  - System Architecture & Microservices: [Watch Video 1](https://drive.google.com/file/d/1ZdWTf0Vr3xLTXyKjuPojua6WjjOGgT8M/view?usp=drive_link)
  - Containerization & Kubernetes Deployment: [Watch Video 2](https://drive.google.com/file/d/1G9W0oGWvThhTMEMaTpoOF8JCXBKZKhPN/view?usp=drive_link)

---

## 🖼️ System Design Overview

<p align="center">
  <img src="https://github.com/NovelNestHQ/.github/blob/4796da0eb12b38e829acdf1506421fc668360727/assets/system-arch.png" alt="System Architecture Diagram" width="700"/>
</p>

---

## 🚀 Getting Started

To run the full application locally or on Minikube, refer to the [k8s-manifests README](https://github.com/NovelNestHQ/k8s-manifests) for deployment steps using:

- `deploy-all.sh`: Deploys all services in order
- `kubectl apply -f <service>`: Apply individual manifests
- `kubectl port-forward`: Access UI, RabbitMQ dashboard, or Kong

---

## 🛠 Technologies Used

- Microservices: Node.js + TypeScript  
- API Gateway: Kong  
- Message Queue: RabbitMQ  
- Databases: PostgreSQL + MongoDB  
- Frontend: React + Vite + TailwindCSS  
- Orchestration: Docker + Kubernetes (Minikube)  
- Auth: SuperTokens  
- CI/CD (optional): GitHub Actions + Quay.io Registry  

---

> 💡 For more details, walkthroughs, and advanced Kubernetes deployments, refer to the full [📘 technical document](https://drive.google.com/file/d/1Vxrej8pZAZvGbFhOCBFYtVUE-BPhsiUa/view?usp=drive_link).

---

