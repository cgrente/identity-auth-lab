# identity-auth-lab

## Status
🚧 **Work in Progress — Actively being developed**

This repository is intentionally public early to document  
**design decisions, architecture, and security tradeoffs** as the system evolves.

The goal is not speed, but correctness and clarity around authentication and identity.

---

## Goal

This project is a hands-on laboratory for **modern authentication and identity systems**.

It demonstrates how different authentication mechanisms are **designed, wired, and compared**
— from classic server-side sessions to enterprise-grade OAuth, SAML, and passwordless auth —
with a strong focus on **real-world tradeoffs** rather than toy examples.

The emphasis is on:
- understanding *why* each mechanism exists
- how they interact together
- where each one is appropriate in production systems

---

## Planned Scope

The project will incrementally implement and document:

- **Server-side session authentication**
  - HTTP-only cookies
  - Redis-backed session store
  - CSRF considerations

- **JWT-based authentication**
  - Access tokens vs refresh tokens
  - Token rotation and expiration strategies
  - Stateless API authorization

- **OAuth 2.0 / OpenID Connect**
  - Authorization Code flow with PKCE
  - Separation of login, consent, and token issuance
  - First-party and third-party clients

- **Ory Kratos + Ory Hydra**
  - Kratos as identity management (users, credentials, flows)
  - Hydra as OAuth2 / OIDC provider
  - Explicit login and consent handling

- **Federated identity**
  - Google Sign-In (OIDC)
  - SAML SSO via an enterprise IdP (e.g. Keycloak)

- **Passwordless authentication**
  - Passkeys / WebAuthn
  - Device-bound credentials
  - Phishing-resistant login flows

Each step will build on the previous one and be fully reproducible via Docker Compose.

---

## Non-Goals

This repository is **not** intended to be:

- A production-ready authentication service
- A polished UI or design-focused frontend
- A framework-specific tutorial (e.g. “how to use X auth library”)
- A copy-paste boilerplate for real deployments

Instead, it focuses on **principles, flows, and architecture**, even when that means
writing more code than a shortcut library would require.

---

## Guiding Principles

- Prefer **explicit flows** over magic abstractions
- Treat authentication and authorization as separate concerns
- Make security tradeoffs visible and documented
- Optimize for learning and correctness, not minimal code

---

## Current Phase

**Phase 0 — Infrastructure & Identity Wiring**

- Docker-based local environment
- OAuth login and consent plumbing
- Token issuance validation

Application logic will be added once the identity backbone is proven to work end-to-end.
