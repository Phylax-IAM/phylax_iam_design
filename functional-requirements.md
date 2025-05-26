## 📝 Functional Requirements

These requirements describe the core behavior of the application.

- ### 🛡️ Authentication
    - Default and custom token structure and validation flow structure based on token policy (not fixed might use something better if exists).
    - Support for email/username/phone number + password authentication (Configurable per tenant).
    - Secure password hashing.
    - Default and custom password policy enforcement.
    - Account lockout after configurable failed login attempts.
    - Last Failed or successful login data history.
    - Offer Captcha logic for all the requests
    - Support for TOTP(Time based One Time Password).
    - Support for multiple channel base TOTP.
    - Support for all major MFA providers and open to add new.
    - Support for all major OAuth2 providers and open to add new.
    - Support for all major SSO (Single Sign on) providers and open to add new.
    - Secure redirect URI validation.
    - Token revocation and introspection endpoints.
    - Multiple token type support (auth, refresh, API Key, custom).
    - Support for association API Keys with system users/applications/etc.
    - Metadata tagging for API Keys (e.g. purpose, usage).
    - 

- ### ✍🏽 Authorization

- ### 👶🏽 User Management

- ### 🚦 Role and Permission Management

- ### 👥 Group Management

- ### 🪖 Security Features

- ### 🏢 Multi-Tenancy
    - Dynamic client registration per tenant.
    - Tenant specific password policy support.
    - Support for custom OIDC/Oauth2 IdPs per tenant.
    - Each tenant must have isolated authentication configurations.
    - Support for both default and tenant-specific authentication policies.
    - Scoped authentication (users must authenticate within the correct tenant context).
    - Ability to onboard and configure authentication methods per tenant.
    - Ability to roll in and out new configure authentication methods per tenant using smooth transition flows (like allow users to be authenticated using the old or the new methods for a brief window days-weeks).

- ### 📆 Scheduled Jobs

- ### 🔔 Notifications
