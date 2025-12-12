---
title: Authentication Methods
deprecated: false
hidden: false
metadata:
  robots: index
---
This section describes the authentication mechanisms supported by Akeyless. Authentication defines **how an identity proves who it is** before any authorization decisions are evaluated.

Akeyless supports a broad set of authentication methods for both human users and machine workloads. Each method results in an authenticated identity that is later evaluated by authorization policies (RBAC, ABAC, ownership, and Universal Identity).

This section focuses on *what authentication methods exist* and *when to use them*, not on authorization behavior.

## Supported Authentication Methods

### Username and Password
Interactive authentication for individual users, primarily used for initial access and console login.

### Single Sign-On (SSO)
Integration with external identity providers using OIDC or SAML. Commonly used for enterprise users and centralized identity management.

### API Keys
Static credentials used for non-interactive access such as automation, CI/CD pipelines, and scripts.

### Kubernetes Authentication
Workload authentication using Kubernetes Service Account tokens. Commonly used for in-cluster applications and Kubernetes-native integrations.

### Cloud Provider IAM
Authentication using native cloud identity mechanisms:
- AWS IAM
- Azure Active Directory
- Google Cloud IAM
- Oracle Cloud Infrastructure (OCI IAM)

These methods eliminate static credentials and rely on cloud-native identity.

### LDAP and Active Directory
Authentication against directory services for organizations with on-premises or hybrid identity infrastructure.

### Kerberos
Ticket-based authentication for environments that rely on Kerberos-backed identity systems.

### Universal Identity (Identity Mapping)
Universal Identity is not an authentication mechanism itself. It maps multiple authentication methods to a single logical identity for consistent authorization and governance.

---

## Choosing an Authentication Method

Authentication methods are selected based on:
- Human vs workload access
- Interactive vs non-interactive usage
- Cloud-native vs on-premises environments
- Credential rotation and lifecycle requirements

Authentication determines *who you are*, while authorization determines *what you can do*.

---

## Next Steps

This sections provides detailed guidance on configuring and using each authentication method.
