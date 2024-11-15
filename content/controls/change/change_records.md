---
title: Change Records
level: 1
weight: 10
control_code: KCC1
tldr: All systems and services maintain a record of changes
rationale: To meet our change management requirements, all changes to production systems are recorded permanently
areas: 
 - change
---

# {{% param "title" %}}
{{< area_head >}}

## Background

The deployment steps in our pipelines automatically log all deployments, and we can also control that we only deploy software that is approved in the {{% param "csor"  %}} audit trail.

{{< figure src="/images/change-records.svg" alt="Change records" >}}

## How we implement this control

* We monitor production systems and automatically record a forensic history of all changes in Kosli using [environment monitoring](https://docs.kosli.com/getting_started/environments/)
    * Environment records can be found here: https://app.kosli.com/kosli/environments/
