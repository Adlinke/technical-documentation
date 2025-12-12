---
title: Accessing Akeyless with a CLI
deprecated: false
hidden: false
metadata:
  robots: index
---
CLI access allows users and automation to interact with Akeyless using the command-line interface. The CLI provides a convenient wrapper around the Akeyless API for scripting, development, and operational workflows.

CLI access uses the same authentication and authorization mechanisms as API access.

## Typical Use Cases

CLI access is commonly used for:

- Local development and testing
- Operational tasks
- Scripting and automation
- CI/CD pipelines
- Debugging and troubleshooting access issues

---

## Authentication Behavior

The CLI supports multiple authentication methods, including:

- API keys
- SSO and interactive login flows
- Kubernetes authentication
- Cloud IAM authentication

Authentication credentials are stored locally according to CLI configuration and profile settings.

---

## Authorization Enforcement

All CLI operations are subject to the same authorization policies as API access:

- RBAC and ABAC policies
- Ownership rules
- Conditional access enforcement

The CLI does not bypass or modify authorization behavior.

---

## Profiles and Configuration

The CLI supports profiles to manage multiple identities and environments:

- Profiles allow switching between accounts or access methods
- Configuration files store non-secret settings
- Sensitive credentials should be protected using OS-level security controls

---

## Relationship to API and SDKs

The CLI is a thin wrapper around the Akeyless API:

- Every CLI command maps directly to API calls
- Authorization behavior mirrors API responses
- SDKs use the same underlying APIs

Understanding API access helps in understanding CLI behavior.

---

## Key Characteristics

- Command-line driven
- Suitable for both humans and automation
- API-backed
- Consistent authorization behavior

---

## Summary

CLI access provides a flexible and scriptable way to interact with Akeyless. It leverages the same API and policy enforcement model as other access paths while offering a developer-friendly interface.
