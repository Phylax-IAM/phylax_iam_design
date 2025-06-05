# 🖥️ System Design: Phylax IAM

---

## 🎯 Overview

- Phylax is a secure, multi-tenant Identity and Access Management (IAM) system that provides authentication and authorization solutions, including OAuth2, API key support, Multi-Factor Authentication (MFA), RBAC, and ABAC. It can integrate seamlessly with any application or operate as a standalone service.
  
- Phylax addresses the complexities of managing secure, scalable authentication and authorization across multiple applications and tenants. It simplifies user access control, ensuring organizations can easily enforce security policies while maintaining flexibility and compliance with varying business needs.
  
- Phylax provides a unified IAM solution for managing users, roles, and permissions, with customizable security policies for multiple tenants. It offers centralized control over user access, authentication, and authorization, supporting both default and tenant-specific configurations.
  
---

## 📝 Functional Requirements

- [Functional Requirements](./functional-requirements.md)

---

## ⌛️ Non-Functional Requirements

- High Scalability (Horizontal and Vertical)
- High Availability
- Low To Mid Latency (as low as possible)
- High Consistency
- High Security
- Cost Efficient

---

## 🏛️ High-Level Architecture

- [System Context Design](./Diagrams/img/system-context.design.png)
- [Data Flow Design](./Diagrams/img/data-flow.design.png)

---

## 🧇 Component Breakdown

Break down each major part (e.g., API Gateway, Auth Service, URL Service, Analytics Service):

- [Aegis - API Gateway Service](./Services/Aegis%20-%20API%20Gateway%20Service/)
- [Praeventus - API Firewall Service](./Services/Praeventus%20-%20API%20Firewall%20Service/)
- [Clavis - OAuth Service](./Services/Clavis%20-%20OAuth%20Service/)
- [Probatio - MFA Service](./Services/Probatio%20-%20MFA%20Service/)
- [Signum - Token Service](./Services/Signum%20-%20Token%20Service/)
- [Persona - User Service](./Services/Persona%20-%20User%20Service/)
- [Cohortis - Group Service](./Services/Cohortis%20-%20Group%20Service/)
- [Ordinis - RBAC Service](./Services/Ordinis%20-%20RBAC%20Service/)
- [Patronus - Tenant Service](./Services/Patronus%20-%20Tenant%20Service/)
- [Kronos - Scheduled Jobs Service](./Services/Kronos%20-%20Scheduled%20Jobs%20Service/)
- [Symphonos - API Composition Service](./Services/Symphonos%20-%20API%20Composition%20Service/)
- [Hermes - Notification Service](./Services/Hermes%20-%20Notification%20Service/)
- [Fidelis - Application Service](./Services/Fidelis%20-%20Application%20Service/)

---

## 📞 Communication Flow

- Sequence diagram for common flows (e.g., short URL creation, redirect)
- Message/event flow (Kafka topics, queues, etc.)

---

## 🚨 Security Considerations

- Authentication (OAuth2, JWT, API keys, etc.)
- Authorization model (RBAC, ABAC)
- Rate limiting, abuse protection
- Data encryption (at rest/in transit)

---

## 📦 Deployment & Infrastructure

- CI/CD overview
- Docker, Kubernetes setup
- Horizontal/vertical scaling
- Cloud provider setup (if any)

---

## 🔎 Observability & Reliability

- Logging, metrics, tracing
- Health checks
- Alerts/monitoring tools

---

## 📑 Related Documents

- [API specs](./api-specs.yaml)
- [Changelog](./changelog.md)
