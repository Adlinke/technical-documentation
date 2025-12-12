---
title: Authorization, Policies, and Governance
deprecated: false
hidden: false
metadata:
  robots: index
---
This section describes how Akeyless determines **what authenticated identities are allowed to do**, how those decisions are enforced, and how access is governed over time.

In Akeyless, authorization, policy evaluation, and governance are not separate systems. They are part of a single access control model that consistently enforces permissions across users, workloads, environments, and access paths.

This section explains how access decisions are made, how policies are structured, and how organizations govern access at scale.

---

## What Authorization Means in Akeyless

Authorization in Akeyless answers the question:

> **What actions is this identity allowed to perform on which resources, and under what conditions?**

Authorization is evaluated after authentication has established identity. Once authenticated, every request is subject to policy evaluation before it is allowed or denied.

Authorization behavior is consistent regardless of whether access occurs through:
- The web console
- APIs
- CLI tools
- SDKs
- Gateways or private environments

---

## Policy-Centric Access Control

Akeyless uses a policy-centric model. All authorization decisions are enforced through policies that define:

- Which resource paths can be accessed
- Which operations are permitted (read, create, update, delete, list, etc.)
- Conditional rules that restrict access based on context
- Ownership and delegation rules
- How identities are represented and resolved

Policies are evaluated in real time for every request.

---

## Authorization Mechanisms

Akeyless combines multiple mechanisms to provide flexible and precise access control.

### Role-Based Access Control (RBAC)

RBAC defines baseline permissions using roles that grant specific capabilities on defined paths. Roles are reusable and commonly used to enforce least-privilege access for both humans and machines.

---

### Attribute-Based Access Control (ABAC)

ABAC extends RBAC with conditional logic. Policies can restrict access based on attributes such as identity properties, environment, time, network context, or request metadata.

RBAC and ABAC are evaluated together during authorization.

---

### Ownership and Personal Folders

Ownership-based access allows users to control resources they own without requiring explicit role assignments. Personal Folders use ownership rules to separate private and shared resources.

Ownership rules complement, but do not replace, role-based policies.

---

### Universal Identity

Universal Identity is an authorization abstraction that maps multiple authentication methods to a single logical identity. This enables consistent policy enforcement and governance even when the same workload or user authenticates using different mechanisms across environments.

Universal Identity does not authenticate identities; it governs how authenticated identities are represented and authorized.

---

## Governance in Akeyless

Governance defines how access policies are designed, managed, reviewed, and evolved over time. In Akeyless, governance is enforced through policy structure and operational practices rather than manual controls.

Key governance principles include:
- Least-privilege access
- Separation of duties
- Environment and namespace isolation
- Clear ownership and delegation
- Auditability and review

Governance applies uniformly across all access paths and environments.

---

## Policy Lifecycle

Effective access control requires managing the full policy lifecycle:

1. Designing policies and roles
2. Assigning access to identities
3. Enforcing policies during runtime
4. Reviewing access and audit activity
5. Troubleshooting and remediating issues

This section covers both the mechanics of policy evaluation and practical guidance for maintaining secure access over time.

---

## Subsections

This section includes the following focused pages:

- **Policy Evaluation** – How policies are evaluated, ordered, and enforced
- **Policy Troubleshooting** – How to diagnose and resolve authorization issues

---

## Next Steps

Understanding authorization, policies, and governance is essential for operating Akeyless securely at scale. The following pages provide detailed guidance on policy behavior and troubleshooting access decisions.
