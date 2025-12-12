---
title: Authorization Models
deprecated: false
hidden: false
metadata:
  robots: index
---
This section describes how Akeyless evaluates **who can access what**, and under which conditions. Authorization in Akeyless is independent from how an identity authenticates and focuses on enforcing consistent, least-privilege access across users, workloads, and environments.

Authorization decisions are applied after authentication has successfully identified an entity. Once authenticated, Akeyless evaluates authorization models to determine which operations are permitted on secrets, keys, certificates, and other resources.

This section covers the core authorization mechanisms used throughout the platform.

## What Authorization Controls in Akeyless

Authorization governs:

- Which paths an identity can access
- Which operations are allowed (read, create, update, delete, list, etc.)
- Under what conditions access is granted or denied
- How ownership and delegation are enforced
- How access is evaluated consistently across UI, API, and CLI access

Authorization policies apply uniformly, regardless of how an identity authenticated.

---

## Authorization Models Used by Akeyless

Akeyless combines multiple authorization models to provide both flexibility and strong governance.

### Role-Based Access Control (RBAC)

RBAC defines access using roles that grant permissions to specific paths and actions. Roles are reusable, composable, and commonly used to enforce least-privilege access for both humans and machines.

RBAC answers the question:
> *What actions is this identity allowed to perform on which resources?*

---

### Attribute-Based Access Control (ABAC)

ABAC extends RBAC by introducing conditional logic based on attributes such as identity properties, environment, time, network context, or request metadata.

ABAC answers the question:
> *Under what conditions should access be allowed or denied?*

RBAC and ABAC are evaluated together during policy enforcement.

---

### Personal Folders and Ownership

Personal Folders provide ownership-based access separate from role assignments. They are commonly used for individual users, experimentation, or private workspaces.

Ownership-based access determines:
- Default access behavior for user-owned paths
- How personal and shared resources are separated
- When roles should be used instead of ownership

---

### Universal Identity

Universal Identity is an authorization abstraction that allows multiple authentication methods to map to a single logical identity. It provides consistent policy enforcement and governance even when workloads authenticate using different mechanisms across environments.

Universal Identity answers the question:
> *How do we represent and govern identities consistently, regardless of how they authenticate?*

---

## How Authorization Is Evaluated

At a high level, authorization follows this sequence:

1. An identity authenticates using a supported authentication method.
2. The authenticated identity is mapped to a logical identity.
3. RBAC and ABAC policies are evaluated.
4. Ownership rules are applied when relevant.
5. The request is either allowed or denied.

This evaluation process is the same whether access occurs through the web console, API, CLI, or Gateway-mediated workflows.

---

## When to Use Each Model

- **RBAC** for defining baseline permissions and shared access patterns
- **ABAC** for conditional or context-aware access
- **Personal Folders** for user-owned or private resources
- **Universal Identity** for unifying access across authentication methods and environments

Most deployments use a combination of these models.

---

## Next Steps

The following pages in this section describe each authorization model in detail, including configuration options, evaluation behavior, and recommended usage patterns.

Understanding these models is essential for designing secure, scalable access controls in Akeyless.
