---
title: Accessing Akeyless by API
deprecated: false
hidden: false
metadata:
  robots: index
---
API access enables programmatic interaction with Akeyless. All core Akeyless functionality is exposed through a <Glossary>RESTful</Glossary>  API, making API access the foundation for automation, integrations, and higher-level tools.

API access is stateless and designed for machine-to-machine communication

## Typical Use Cases

API access is commonly used for:

* Application secret retrieval
* Automation and CI/CD pipelines
* Infrastructure provisioning
* Custom integrations
* SDK and CLI implementations

***

## Authentication Behavior

API access supports all non-interactive authentication methods, including:

* API keys
* Kubernetes authentication
* Cloud provider IAM authentication
* LDAP, Kerberos, and directory-based authentication
* Universal Identity mapping, when configured

Authentication results in a token or signed request that identifies the caller.

***

## Authorization Enforcement

API requests are evaluated against the same authorization policies as all other access paths:

* RBAC and ABAC policies
* Ownership rules
* Conditional access controls

Authorization decisions are enforced per request.

***

## Stateless Request Model

API access is stateless:

* Each request is authenticated independently
* No server-side session is maintained
* Tokens and credentials must be supplied with each request

This model is well-suited for distributed systems and automation.

***

## Error Handling

Authorization failures return explicit error responses, such as:

* Authentication errors
* Permission denied errors
* Policy condition failures

These errors are consistent across API, CLI, and SDK usage.

***

## Key Characteristics

* Programmatic and machine-oriented
* Stateless
* Foundation for CLI and SDKs
* Fully auditable

***

## Summary

API access provides the core interface for interacting with Akeyless programmatically. It enforces strict authentication and authorization on every request and serves as the basis for all automation and integration workflows.
