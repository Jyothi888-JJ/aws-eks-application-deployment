# AWS EKS Application Deployment

## 📌 Project Overview

This project demonstrates how to deploy a containerized application on **Amazon EKS (Elastic Kubernetes Service)** using Kubernetes manifests.

The project uses Kubernetes **Namespace, Deployment, Service, and ConfigMap** resources to manage and expose the application.

---

## 🏗️ Architecture

```text
                Amazon EKS
                    │
                    │
              ┌─────▼─────┐
              │ Namespace  │
              │ devops-demo│
              └─────┬─────┘
                    │
             ┌──────▼──────┐
             │ Deployment  │
             │ 2 Replicas  │
             └──────┬──────┘
                    │
             ┌──────▼──────┐
             │   Service   │
             │ LoadBalancer│
             └──────┬──────┘
                    │
                Application
```

---

## ☁️ AWS Services

* Amazon EKS
* Elastic Load Balancing

## 🛠️ Technologies

* Kubernetes
* Docker
* YAML
* Nginx
* kubectl

---

## 📂 Project Structure

```text
aws-eks-application-deployment/
│
├── README.md
├── deployment.yaml
├── service.yaml
├── namespace.yaml
├── configmap.yaml
└── screenshots/
```

---

## ⚙️ Kubernetes Resources

### Namespace

Creates an isolated Kubernetes namespace:

```text
devops-demo
```

### Deployment

The Deployment runs **2 replicas** of the Nginx application.

```text
Deployment
    ↓
2 Pods
    ↓
Nginx Containers
```

### Service

A Kubernetes `LoadBalancer` Service exposes the application externally.

### ConfigMap

Stores non-sensitive application configuration such as:

```text
APP_ENV=production
APP_NAME=devops-demo
```

---

## 🔄 Deployment Flow

```text
Kubernetes YAML Manifests
          ↓
     kubectl apply
          ↓
       Namespace
          ↓
      Deployment
          ↓
       2 Pods
          ↓
       Service
          ↓
    LoadBalancer
          ↓
     Application
```

---

## 🎯 Key Concepts Demonstrated

* Amazon EKS
* Kubernetes Deployments
* Kubernetes Pods
* Kubernetes Services
* LoadBalancer Services
* Kubernetes Namespaces
* ConfigMaps
* Replica management
* Kubernetes YAML manifests
* Application exposure using Kubernetes Services

---

## 🚀 Future Improvements

* Add Kubernetes Ingress
* Add Helm charts
* Add Horizontal Pod Autoscaler (HPA)
* Add resource requests and limits
* Add liveness and readiness probes
* Deploy a custom Docker image
* Add GitHub Actions CI/CD
* Add AWS Load Balancer Controller

---

## 📌 Project Purpose

This project is part of my **AWS DevOps portfolio** and demonstrates practical knowledge of deploying and managing containerized applications using **Amazon EKS and Kubernetes**.
