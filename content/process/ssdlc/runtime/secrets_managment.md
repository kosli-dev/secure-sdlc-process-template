---
title: Secrets Management
level: 1
weight: 30
tldr: Build and runtime secrets are stored securely and documented appropriately
rationale: Leaked secrets such as api keys, cryptography keys, identity tokens
  are a common attack scenario.
---
# {{% param "title" %}}
{{< area_head >}}

## Background

Secrets must be stored in a secure way, and a documented in a central place.
[Cryptographic failures are the second highest risk in the OWASP top ten](https://owasp.org/Top10/A02_2021-Cryptographic_Failures/) so rigor and process is essential.

{{< figure src="/images/secrets-management.svg" alt="Change Records" >}}