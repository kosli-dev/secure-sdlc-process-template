---
title: System Access Controls
level: 1
weight: 40
control_code: KCC4
tldr: All access to runtime environments requires authentication and audit trails
rationale: To meet our system access control policy, all access must be approved and auditable
areas: 
 - change
---

# {{% param "title" %}}
{{< area_head >}}

## Background

As part of normal software development, it can be necessary to gain remote access to runtime environments.  This can be for many reasons:

* Debugging the runtime environment
* Running migration scripts
* Inspecting the behaviour of running systems

This must be limited to authorized personnel and all activities performed should have full audit trails.

## How we implement this control

* Any remote shell session require SSO authentication and full adit trails are logged in Kosli here: https://app.kosli.com/kosli/audit-trails
* This forms part of our [System Access Control Policy](https://app.drata.com/policy-builder/18)
* All access audit trails are reviewed