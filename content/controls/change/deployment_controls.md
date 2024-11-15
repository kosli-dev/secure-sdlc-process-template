---
title: Deployment Controls
level: 1
weight: 20
control_code: KCC2
tldr: Deployments controls are enforced in the pipeline and environments
rationale: Ensuring only compliant, approved software deployments are made to production
areas: 
 - change
---
# {{% param "title" %}}
{{< area_head >}}

## Background

We use deployment controls to automatically ensure we only deploy software that
has gone through our Software Development Lifecycle.  This can be implemented as
a gate in the pipeline, or as an admission controller in the environment (ideally
both).

{{< figure src="/images/deployment-controls.svg" alt="Deployment Controls" >}}

## How we implement this control

* We use [Kosli's assert artifact command](https://docs.kosli.com/client_reference/kosli_assert_artifact/) prior to deployment
* We use [Kosli's environment monitoring]({{< ref "workload_monitoring.md" >}}) to alert on non-compliant workloads