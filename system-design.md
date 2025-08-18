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

- [Aegis - API Gateway Service](https://github.com/Phylax-IAM/Aegis.API-Gateway.Design)
- [Praeventus - API Firewall Service]()
- [Clavis - OAuth Service]()
- [Probatio - MFA Service]()
- [Signum - Token Service]()
- [Persona - User Service]()
- [Cohortis - Group Service]()
- [Ordinis - RBAC Service]()
- [Patronus - Tenant Service]()
- [Kronos - Scheduled Jobs Service]()
- [Symphonos - API Composition Service]()
- [Hermes - Notification Service]()
- [Fidelis - Application Service]()

---

## 📞 Communication Flow

- Sequence diagram for common flows (e.g., short URL creation, redirect)
- Message/event flow (Kafka topics, queues, etc.)

---

## 🚨 Security Considerations

- Applications hosted inside VPC
- Authorization model (RBAC, ABAC) to be detailed in the documents for Ordinis.
- Rate limiting, abuse protection to be detailed in Aegis and Praeventus.
- HTTPS connection.

---

## 📦 Deployment & Infrastructure

- Kubernetes Cluster Deployment of the complete application
- Horizontal/vertical scaling
- [CSP Decision Document](./cloud-service-provider-decision.md)

---

## 🔎 Observability & Reliability

- Logging, metrics, tracing
- Health checks
- Alerts/monitoring tools

---

## 📑 Related Documents

- [API specs](./api-specs.yaml)
- [Changelog](./changelog.md)
