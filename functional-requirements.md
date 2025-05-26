## 📝 Functional Requirements

These requirements describe the core behavior of the application.

- ### 🛡️ Authentication
    - Default and custom token structure and validation flow structure based on token policy (not fixed might use something better if exists).
    - Support for Passkey/FIDO2/WebAuthn (biometric devices).
    - Support for email/username/phone number + password authentication (Configurable per tenant).
    - Secure password hashing.
    - Default and custom password policy enforcement.
    - Account temporary / permanent lockout after configurable failed login attempts.
    - Custom Locked account recovery flow.
    - Last Failed or successful login data history.
    - Offer Captcha logic for all the requests.
    - Support for TOTP(Time based One Time Password).
    - Support for Magic link for verification.
    - Support for multiple channel base TOTP.
    - Support for all major MFA providers and open to add new.
    - Support for all major OAuth2 providers and open to add new.
    - Support for all major SSO (Single Sign on) providers and open to add new.
    - Secure redirect URI validation.
    - Token revocation and introspection endpoints.
    - Multiple token type support (auth, refresh, API Key, custom).
    - Support for association API Keys with system users/applications/etc.
    - Metadata tagging for API Keys (e.g. purpose, usage).
    - Issue token combination on successful login.
    - Token revocation logic.
    - Register and manage devices based on fingerprint, user agent etc.
    - Device per user registration.
    - Token per device registration.
    - Tenant specific login and error messages.
    - Default and custom login/logout/authentication flow.
    - Custom forgot password reset flow.
    - Optional tenant configurable account recovery questions.
    - Tenant configurable password history and expiry policy.
    - Link multiple identities (e.g., OAuth + user Data + MFA + SSO).
    - Custom redirect logic per request (accept just the relative path (append to tenant saved front end trusted domain) or complete URL (use Allowlist for containing trusted urls per tenant)).

- ### 👶🏽 User Management

- ### ✍🏽 Authorization

- ### 👥 Group Management

- ### 🚦 Role, Permission & Policy Management

- ### 🪖 Security Features
    - Detect and Block Bots.
    - Enforce CORS, CSRF, etc.
    - Captcha for brute force attempts.
    - Global and tenant base rate limiting (two layers) for protection against DDOS like attacks.

- ### 🏢 Multi-Tenancy
    - Rate limit per tenant.
    - Tenant custom rate limit base (IP, user, tenant, group, etc).
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

- ### 📜 Documentation
    - Documentation for every service (confluence).
    - OpenAPI documentation for tenant developers(confluence/github/swagger).
    - Link relevant documentation for every page(based on api relevant to it).
