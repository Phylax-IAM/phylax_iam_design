## 📝 Functional Requirements

These requirements describe the core behavior of the application.

- ### 🛡️ Authentication
    - Basic token-based login (JWT)
    - Email + password authentication
    - Secure password storage (hashing with bcrypt/argon2)
    - Basic MFA (TOTP via authenticator app)
    - Login/logout endpoints
    - Token revocation endpoint
    - Token introspection

- ### 👶🏽 User Management
    - User registration (email + password)
    - CRUD operations on user profile
    - User activation/deactivation
    - Soft delete for users
    - Password reset flow via email
    - Store basic user data (name, email, etc.)
    - Fetch pagination list of users

- ### 👥 Group Management
    - Create groups
    - Add/remove users to/from group

- ### ✍🏽 Authorization
    - Define roles (Admin, User, etc.)
    - Assign roles to users
    - Define permissions per role (CRUD - level granularity)
    - Basic access control based on role

- ### 🚦 Role, Permission & Policy Management
    - Static permissions in the format "resource:action" (e.g., user:create, verify:mfa)
    - Create policy engine to implement and support [this json](./templates/policy-structure.json) structure.

- ### 🪖 Security Features
    - Basic rate limiting (global)
    - CORS protection
    - CSRF protection
    - Captcha on login after failed attempts
    - Basic bot protection (e.g., user-agent filtering)

- ### 🏢 Multi-Tenancy
    - Scoped login per tenant
    - Per-tenant user isolation
    - Per-tenant configuration for login methods (enable/disable MFA, etc.)
    - Tenant onboarding (via admin)

- ### 📆 Scheduled Jobs
    - Daily cleanup job (e.g., remove soft-deleted users after x days)
    - Revoked token cleanup
    - Used TOTP cleanup
    - Password expiry reminder after x days

- ### 🔔 Notifications
    - Use queue for consuming events.
    - Use Dequeue for unprocessable event.
    - Send email on any email event triggered for notification type email.

- ### 📜 Documentation
    - Documentation for every service (confluence).
    - OpenAPI documentation for endpoints (swagger).
