# Security Design Document - Phylax IAM

## 1. Overview
-   The purpose of this document is to contain all the security decisions for this application architecture
-   Phylax is an Identity and Access Management Application that can be used out of the box or can be customized for each tenant
-   Authentication & Authorization requirements and policies

## 2. Threat Model
-   DDoS attack protection
-   Trust boundary (cloud VPC)
-   Protecting user's private data
-   Single point of entry trough [API Gateway](./Services/Aegis%20-%20API%20Gateway%20Service/) & [Firewall Service](./Services/Praeventus%20-%20API%20Firewall%20Service/)

## 3. Authentication
-   Trusted identity providers
    -   OAuth2
    -   MFA
-   Token handling
    -   JWT
    -   Auth & refresh token
    -   API Key
    -   Revoked token list
    -   Token payload must never contain sensitive info, it should only contain the minimum required information
-   Credential management 
    -   Never store any sensitive information in plain text
    -   Tenants should never be even aware of any information out of there scope or related to the other tenants
-   Password policies
    -   Hashing user passwords with radom salt
    -   password expiry
    -   password history
    -   password structure

## 4. Authorization
-   Fixed static permissions
-   Dynamic Roles and policies
-   Role Based Access Control
-   Attribute Based Access Control
-   Least access principle

## 5. Network Security
-   TLS (HTTPS) termination at API Gateway inside the VPC
-   Only the API Gateway service is allowed to have an open connection outside the VPC
-   Firewall service will be right behind the API Gateway service

## 6. Data Protection
-   Encryption in transit (TLS, HTTPS)
-   Encryption at rest (AWS KMS)

## 7. Secrets Management
-   Secrets Management (AWS Secrets Manager)
-   Rotation policies

## 8. Auditing & Logging
-   Log types
    -   Auth logs
    -   Request logs
    -   Access logs
-   Log destinations (Cloudwatch, Elasticsearch, S3, any external service)
-   Log retention (1 year) default and privacy
-   Tracer injection policies
    -   Frequency
    -   Payload

## 9. Known Risks & Mitigations
-   Cross Site Request Forgery - CSRF Token
-   Cross Origin Resource Sharing
-   DDoS protection - Rate limiting (Global)
-   Abuse detection and logging

## 10. Security Diagram
-   [Security Design Diagram](./Diagrams/img/security.design.png)