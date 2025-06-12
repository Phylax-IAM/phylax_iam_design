# Phylax IAM Design Repository

<p align="center">
    <img src="./logo/Phylax IAM Logo.png" alt="Phylax IAM Logo" width="400"/>
</p>

---

📘 **Central source for architecture and API design docs for Phylax IAM system**

---

## 🧩 What Is This Repository?

This repository holds all **design artifacts** related to the **Phylax IAM** suite, specifically focused on the **Symphonos** composition layer and its API contract. It includes:

- High-level architecture and component diagrams  
- Unified API endpoint specification for MVP release  
- Data models, sequence diagrams, and security flows
- Start looking here: [System Design Document](./system-design.md)  

---

## 📂 Folder Structure

```text
/
├── Diagrams/                                   
│   ├── draw.io/                               
│   |   ├── data-flow.design.dio               
│   |   ├── high-level.design.dio              
│   |   ├── security.design.dio                
│   |   └── system-context.design.dio          
|   └── img/                                   
│       ├── data-flow.design.png               
│       ├── high-level.design.png              
│       ├── security.design.png                
│       └── system-context.design.png          
│
├── CHANGELOG.md                                
├── cloud-service-provider-decision.md           
├── domain-design.md                             
├── functional-requirements.md                  
├── microservices-design.md                     
├── security-decision.md                        
├── system-design.md                              
└── README.md                                 
```

---

## ✅ Getting Started

1. **Clone the Repo**

   ```bash
   git clone https://github.com/Phylax-IAM/phylax_iam_design.git
   ```

2. **Explore the Design Docs**

   * Diagrams in `/Diagrams/img/`
   * Logos in `/logo/`

3. **Your Feedback & Contributions**

   * Hit the Issues tab or open a PR

---

## 📋 Key Documents Explained

* **`system-design.md`** – Serves as the primary reference for all high-level architectural decisions, system context, and component interactions within the Phylax IAM platform.
  
* **`microservices-design.md`** – Details the architectural rationale and design principles followed for each microservice, including service boundaries, data ownership, and communication patterns.
  
* **`cloud-service-provider-decision.md`** – Outlines the evaluation criteria and justification for selecting the Cloud Service Provider (CSP), considering cost, scalability, security, and operational fit.
  
* **`security-decision.md`** – Documents all security-related architectural choices such as authentication mechanisms, token management, encryption standards, threat models, and mitigation strategies.

---

## 🛠 How to Use These Docs

* As a **reference for frontend/backend implementation**
* For **auto-generating mock servers or tests** from OpenAPI spec
* To maintain **naming/response consistency across phases**
* As source-of-truth during architecture reviews or onboarding

---

## 🤝 Contributing

Please follow these conventions:

* Write clear and consistent API/field names
* Add diagrams or descriptions when changing or introducing new endpoints
* Use [Conventional Commit Messages](https://www.conventionalcommits.org/en/v1.0.0/)

---

## 📄 License

[MIT License](./LICENSE) – See LICENSE file for details.

---

## 🔗 Contacts

For questions or feedback, reach out to:

* **Authored by**: *Pragyanshu Rai* (`<pragyanshu.rai.phylax.iam@gmail.com>`)
* **Project Lead**: **Pragyanshu Rai**