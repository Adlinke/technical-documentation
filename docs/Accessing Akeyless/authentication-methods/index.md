---
title: Authentication Methods
deprecated: false
hidden: false
metadata:
  robots: index
---
This section describes the authentication mechanisms supported by Akeyless. Authentication defines **how an identity proves who it is** before any authorization decisions are evaluated.

Akeyless supports a broad set of authentication methods for both human users and machine workloads. Each method results in an authenticated identity that is later evaluated by authorization policies (RBAC, ABAC, ownership, and Universal Identity).

This section focuses on _what authentication methods exist_ and _when to use them_, not on authorization behavior.

## Supported Authentication Methods

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Authentication Method
      </th>

      <th>
        Description
      </th>

      <th>
        Sub-Options Available
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Username and Password
      </td>

      <td>
        Interactive authentication for individual users, primarily used for initial access and console login.
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        API Keys
      </td>

      <td>
        Static credentials used for non-interactive access such as automation, CI/CD pipelines, and scripts.
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Single Sign-On (SSO)
      </td>

      <td>
        Integration with external identity providers using OIDC or SAML. Commonly used for enterprise users and centralized identity management.
      </td>

      <td>
        * OIDC
        * SAML
      </td>
    </tr>

    <tr>
      <td>
        Kubernetes
      </td>

      <td>
        Workload authentication using Kubernetes Service Account tokens. Commonly used for in-cluster applications and Kubernetes-native integrations.
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Cloud Provider IAM
      </td>

      <td>
        Authentication using native cloud identity mechanisms.
      </td>

      <td>
        * AWS IAM
        * Azure Active Directory
        * Google Cloud IAM
        * Oracle Cloud Infrastructure (OCI IAM)
      </td>
    </tr>

    <tr>
      <td>
        LDAP and Active Directory
      </td>

      <td>
        Authentication against directory services for organizations with on-premises or hybrid identity infrastructure.
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Kerberos
      </td>

      <td>
        Ticket-based authentication for environments that rely on Kerberos-backed identity systems.
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Universal Identity (Identity Mapping)
      </td>

      <td>
        Universal Identity is not an authentication mechanism itself. It maps multiple authentication methods to a single logical identity for consistent authorization and governance.
      </td>

      <td>

      </td>
    </tr>
  </tbody>
</Table>

***

## Next Steps

This sections provides detailed guidance on configuring and using each authentication method.
