# Fells Code LLC

Fells Code LLC is a software company focused on building secure, reliable authentication and infrastructure tooling for modern applications.

We specialize in **passwordless authentication systems**, developer-focused APIs, and operational tooling that emphasizes clarity, security, and production-ready design. Our products are built to be explicit, inspectable, and deployable without vendor lock-in.

---

## Focus Areas

Fells Code builds software in the following domains:

- Passwordless authentication and identity infrastructure
- Developer tooling and APIs
- Self-hosted and open source systems
- Security-first application architecture
- Production-shaped local development workflows

Our work prioritizes correctness, transparency, and long-term maintainability over abstraction and convenience layers that obscure system behavior.

---

## Products and Projects

### Seamless Auth

Seamless Auth is a passwordless authentication system designed to be embedded directly into applications. It avoids redirects, third-party hosted identity flows, and client-side token handling in favor of explicit, server-validated sessions.

**Core projects:**

- **Seamless Auth Server**  
  https://github.com/fells-code/seamless-auth-api  
  The authentication server responsible for verification, session issuance, and identity state.

- **Seamless Auth API (Core)**  
  https://github.com/fells-code/seamless-auth-server/packages/core  
  Framework-agnostic authentication logic used across all integrations.

- **Seamless Auth Express Adapter**  
  https://github.com/fells-code/seamless-auth-server/packages/express  
  Express middleware for authentication and role-based authorization.

- **Seamless Auth React SDK**  
  https://github.com/fells-code/seamless-auth-react  
  Frontend integration for consuming authenticated session state in React applications.

**Key characteristics:**
- Passwordless authentication (OTP, WebAuthn, Passkeys)
- Cookie-based, server-side session validation
- Explicit authentication and authorization boundaries
- Self-hosted and infrastructure-agnostic
- Local development that mirrors production behavior

Documentation:  
https://docs.seamlessauth.com

---

### Seamless Glance

Seamless Glance is a developer-focused operational visibility tool designed to help teams quickly understand and triage cloud infrastructure.

It provides a read-only, terminal-based interface that surfaces high-signal information without requiring deep navigation through provider consoles.

Repositories:  
- https://github.com/fells-code/seamless-glance
- https://github.com/fells-code/seamless-glance-distro

Primary goals:
- Fast infrastructure triage
- Reduced cognitive overhead
- Secure, read-only access
- Clear operational context

---

## Design Philosophy

All Fells Code projects follow a shared set of principles:

- **Explicit over implicit**  
  Systems should be understandable by reading the code and configuration.

- **Security as a baseline**  
  Authentication, authorization, and secrets management are first-class concerns.

- **Production-shaped development**  
  Local development environments should behave like production, not mock systems.

- **Minimal abstraction**  
  Abstractions should clarify behavior, not hide it.

- **Long-term maintainability**  
  We build systems intended to be operated, extended, and audited over time.

---

## Technology Stack

Our products commonly use:

- **Infrastructure:** Docker, Terraform, AWS, IBM
- **Backend:** Node.js, TypeScript, Express, Rust, Python, PostgreSQL
- **Frontend:** React, Vite, Next.js
- **CI/CD:** GitHub Actions, automated release pipelines
- **Security:** Passwordless authentication, signed cookies, JWKS, secrets management

Technology choices are driven by operational clarity and security requirements rather than trends.

---

## Open Source and Licensing

Fells Code maintains both open source and proprietary projects.

Each repository clearly defines its license and usage terms in its own `LICENSE` file. Please refer to individual repositories for specific licensing details.

---

## Contact

Fells Code LLC  
United States  

Website: https://fellscode.com  
Email: contact@fellscode.com  

For partnerships, security inquiries, or collaboration, please reach out via email.

---

Fells Code exists to build software that strengthens the world we all share.
