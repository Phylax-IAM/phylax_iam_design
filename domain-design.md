# 🌐 Domain & Network Design for Phylax

This document outlines the complete structure of domains, subdomains, protocols, and intended usage for the Phylax IAM application. It ensures consistent routing, secure communication, and clear separation of concerns across services.

---

## 🎯 Overview

Phylax is a secure, multi-tenant IAM system. This document defines domain strategy, subdomain allocation, and protocol choices.

---

## 🪪 Application Name

**Phylax**  
Base Domain: `phylax`

---

## 📪 Top Level Domains (TLD) Options & Cost (₹/year)

| TLD      | Price (₹/yr) | Notes         |
|----------|--------------|---------------|
| `.click` | 257/-        | ✅ Selected for initial setup |
| `.in`    | 579/-        | Alternative option |
| `.co.in` | 499/-        | Business usage |
| `.info`  | 86/-         | Cheap, not ideal for production |

**Selected TLD**: `.click`  
**Final Domain**: `phylax.click`

---

## 📮 Subdomains & Their Purpose

| Subdomain     | Full Domain              | Purpose                             |
|---------------|--------------------------|-------------------------------------|
| `api`         | `api.phylax.click`       | Public API Gateway for backend APIs |
| `iam`         | `iam.phylax.click`       | IAM frontend portal (e.g., login, register, MFA) |
| `config`      | `config.phylax.click`    | Admin/configuration dashboard (e.g., policy management) |

---

## 🚨 Protocol & Security

| Protocol | Usage     | Notes                            |
|----------|-----------|----------------------------------|
| HTTPS    | Enforced  | TLS terminated at CDN/Gateway    |

All domains use **HTTPS** by default. TLS certificates managed via **Let's Encrypt**, **Cloudflare**, or custom provider.

---

## 🚏 Routing & Architecture Summary

- All requests go through a **API Gateway or CDN (e.g., Aegis, AWS Cloudfront)**.
- Subdomains are mapped to different services/micro frontend.
- Backend services reside behind the `api` domain and are routed via API Gateway.

