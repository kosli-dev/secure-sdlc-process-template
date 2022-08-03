---
title: Change Records
level: 1
weight: 10
tldr: All systems and services maintain a record of changes
rationale: To meet our change management requirements, all changes to production systems are recorded permanently
---

# {{% param "title" %}}
{{< area_head >}}

## Background

The deployment steps in our pipelines automatically log all deployments, and we can also control that we only deploy software that is approved in the {{% param "csor"  %}} audit trail.

{{< figure src="/images/change-records.svg" alt="Change records" >}}