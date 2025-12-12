---
title: Access Paths
deprecated: false
hidden: false
metadata:
  robots: index
---
This section describes **how authenticated identities interact with Akeyless**. While authentication determines identity and authorization determines permissions, access paths define *how requests are made* and *how policies are enforced in practice*.

Akeyless supports multiple access paths, each designed for different users and workflows.

## Supported Access Paths

### Web Browser Access
Human users interact with Akeyless through the web-based Console. Browser access is session-based and subject to the same authorization policies as all other access paths.

### API Access
Programmatic access using the Akeyless REST API. API access is stateless, token-based, and commonly used by automation, services, and integrations.

### CLI Access
The Akeyless CLI provides a command-line interface for interactive use, scripting, and operational workflows. CLI access uses the same authentication methods and APIs as other access paths.

### SDK Access
Language-specific SDKs (such as Go, Python, Java, and JavaScript) provide native bindings for the Akeyless API. SDKs do not introduce new access semantics; they are wrappers around API access and enforce the same authentication and authorization rules.

---

## Policy Enforcement Across Access Paths

Authorization behavior is consistent across all access paths:
- Web Console
- API
- CLI
- SDKs
- Gateway-mediated access

Differences between access paths relate to *interaction style* and *user experience*, not to security controls.

---

## Next Steps

This section describes each access path in detail, including authentication flows, permission behavior, and common usage patterns.
