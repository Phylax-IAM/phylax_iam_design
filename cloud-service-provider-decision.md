
## 📄 Cloud Service Provider (CSP) Selection Decision Document

### Document Title: **Cloud Service Provider Evaluation & Final Decision**

**Project Name**: *Phylax IAM Platform*
**Author**: *Pragyanshu Rai*
**Date**: *2025-06-05*
**Version**: *v1.0*

---

### 1. **Objective**

To select the most appropriate Cloud Service Provider (CSP) to host and manage the **Phylax IAM** platform secure, multi-tenant Identity and Access Management system supporting OAuth2, MFA, RBAC, ABAC, and API key validation.

---

### 2. **Evaluation Criteria**

| Category         | Criteria                                                             |
| ---------------- | -------------------------------------------------------------------- |
| Cost             | Free Tier, Pay-as-you-go pricing, long-term commitment discounts     |
| Global Reach     | Availability across multiple regions, especially Asia-Pacific and EU |
| Compliance       | Support for GDPR, HIPAA, ISO 27001                                   |
| Security         | IAM, encryption at rest/in-transit, audit logs                       |
| Service Maturity | Managed services for containers, databases, serverless               |
| Ecosystem        | SDKs, DevOps tooling, marketplace integrations                       |
| SLA              | >= 99.99% uptime guarantee for core services                         |
| Vendor Lock-in   | Ability to adopt multi-cloud/hybrid in the future                    |
| Support          | Availability of premium support and incident response                |

---

### 3. **CSPs Considered**

#### 🟩 AWS (Amazon Web Services)

* Pros:

  * Mature services (e.g., IAM, EKS, Lambda, KMS)
  * Broad regional availability
  * Granular IAM & policy management
  * Compliance-ready
  * I have prior knowledge and experience
* Cons:

  * ~~Slightly steeper learning curve~~ (Already have experience)
  * Higher pricing for some managed services (Free Tier for most as the application is not expected to face a lot of traffic)

#### 🟦 Azure

* Pros:

  * Strong enterprise integration (Active Directory, Office 365)
  * Good CI/CD support via GitHub Actions
* Cons:

  * Less mature Kubernetes support
  * Slight lag in OSS-native services

#### 🟥 Google Cloud Platform (GCP)

* Pros:

  * Excellent Kubernetes (GKE), IAM
  * Per-second billing, generous free tier
* Cons:

  * Smaller global footprint
  * Fewer enterprise support integrations

---

### 4. **Comparative Matrix**

| Feature              | AWS       | Azure     | GCP        |
| -------------------- | --------- | --------- | ---------- |
| IAM granularity      | ✅ Best    | ✅ Good    | ✅ Good     |
| Kubernetes (Managed) | ✅ Mature  | ⚠️ Okay   | ✅ Best     |
| Serverless offerings | ✅ Lambda  | ✅ Funcs   | ✅ Cloud Fn |
| Compliance readiness | ✅ Full    | ✅ Full    | ✅ Partial  |
| Global regions       | ✅ 30+     | ✅ 25+     | ⚠️ \~20    |
| Support              | ✅ Premium | ✅ Premium | ✅ Premium  |
| Lock-in risk         | ⚠️ High   | ⚠️ High   | ✅ Low      |
| Pricing model        | ⚠️ High   | ⚠️ Medium | ✅ Low      |

---

### 5. **Final Decision**

🟩 **Selected Provider**: **Amazon Web Services (AWS)**

**Reasoning**:

* Offers the most mature IAM and RBAC stack, essential for **Phylax IAM**
* Provides granular access policies (STS, roles, fine-grained permissions)
* Proven compliance support (SOC 2, ISO, GDPR, etc.)
* Excellent support for containerized workloads and future serverless migration
* Large-scale community and enterprise trust
* Previous experience and knowledge

---

### 6. **Risks and Mitigations**

| Risk                      | Mitigation Strategy                                     |
| ------------------------- | ------------------------------------------------------- |
| Vendor Lock-in            | Use container-based services with Terraform             |
| Cost creep                | Regular cost monitoring via AWS Budgets & Cost Explorer |
| Service limits/throttling | Request quota increases; design for autoscaling         |
| Regional outages          | Multi-AZ, multi-region deployment strategy              |

---

### 7. **Future Considerations**

* Explore multi-cloud compatibility via Kubernetes abstraction layer
* Evaluate Azure AD integration for B2B scenarios
* Periodic review every 12 months or after major service incidents

---

### 8. **Approval**

| Name           | Role            | Date       | Signature |
| -------------- | --------------- | ---------- | --------- |
| Pragyanshu Rai | Lead Architect  | 2025-06-05 | \[Signed] |


