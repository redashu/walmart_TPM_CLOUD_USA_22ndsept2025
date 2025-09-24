# Service Mesh Overview

## 🤔 What is a Service Mesh?

A service mesh is an infrastructure layer that manages communication between microservices in a distributed application.

Instead of each microservice having to handle service discovery, retries, security, logging, and observability itself, a service mesh handles it through a sidecar proxy (usually Envoy).

**Key Benefit**: The app code focuses on business logic, while the mesh handles service-to-service communication.

## ✨ Key Features of a Service Mesh

### 🚦 Traffic Management
- Load balancing
- Routing
- Retries
- Failover

### 🔒 Security
- mTLS (mutual TLS) for service-to-service encryption
- Authentication & Authorization between services

### 📊 Observability
- Distributed tracing
- Metrics
- Logging for all service calls

### ⚖️ Policy Control
- Rate limits
- Quotas
- Access rules
- Circuit breakers

## ⚙️ How It Works

1. A **sidecar proxy** (e.g., Envoy) runs alongside each service container
2. All network traffic goes through the proxy
3. The **service mesh control plane** manages these proxies

## 🏆 Popular Service Mesh Products

### 🟦 Open Source
- **Istio** → Most popular, Envoy-based
- **Linkerd** → Lightweight, Kubernetes-native
- **Consul Connect** (by HashiCorp)
- **Kuma** (by Kong)
- **Open Service Mesh (OSM)** → Microsoft project

### ☁️ Cloud Provider Offerings
- **Google Cloud** → Anthos Service Mesh (built on Istio)
- **AWS** → AWS App Mesh (built on Envoy)
- **Azure** → Azure Service Mesh (preview, often uses OSM or integrates with Istio/Linkerd)
- **Red Hat** → OpenShift Service Mesh (Istio-based)

## ✅ Simple Analogy

Think of a service mesh like **air traffic control for microservices** ✈️:

- **Planes** (microservices) just fly (business logic)
- **ATC** (service mesh) handles routing, safety, visibility, and policies