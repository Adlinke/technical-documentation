---
title: Accessing Akeyless with a Browser
deprecated: false
hidden: false
metadata:
  robots: index
---
Browser access allows human users to interact with Akeyless through a web-based console. This access path is primarily used for administration, configuration, and visibility into secrets, keys, certificates, and access policies.

Browser access is intended for interactive use and follows the same authentication and authorization rules as all other access paths.

## Typical Use Cases

Browser access is commonly used for:

* Initial account setup and onboarding
* Creating and managing secrets, keys, and certificates
* Defining authentication methods and authorization policies
* Reviewing audit logs and activity
* Performing administrative tasks

***

## Authentication Behavior

Browser access supports interactive authentication methods, including:

* Username and password
* Single Sign-On (OIDC or SAML)
* Social Sign-In (Google, GitHub)
* Access Key (also known as API Key)
* Certificate-based authentication

With support for:

* Account Alias
* Universal Identity
* Multi-factor authentication (MFA) using an Authenticator App or Email address

Authentication establishes the user’s identity, which is then evaluated against authorization policies.

***

## Authorization Enforcement

All actions performed through the browser are subject to authorization controls, including:

* Role-Based Access Control (RBAC)
* Attribute-Based Access Control (ABAC)
* Ownership and personal folders
* Universal Identity mapping, when applicable

Permissions in the UI reflect the same policy enforcement used by API and CLI access.

***

## Session Management

Browser access is session-based:

* Sessions are created after successful authentication
* Session lifetime is limited and configurable
* Re-authentication is required after session expiration

Session-based access does not bypass policy enforcement.

***

## Key Characteristics

* Interactive and human-oriented
* UI-driven workflows
* No direct handling of raw credentials after login
* Subject to the same audit logging as other access paths

***

## Summary

Browser access provides a secure, interactive way for users to administer and monitor Akeyless. While optimized for human interaction, it enforces the same authentication and authorization policies as programmatic access paths.
