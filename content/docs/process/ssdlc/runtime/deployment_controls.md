---
title: Deployment Controls
level: 1
weight: 20
tldr: Deployments controls are enforced in the pipeline and environments
rationale: Ensuring only compliant, approved software deployments are made to production
---
# {{% param "title" %}}
{{< area_head >}}

## Background

We use deployment controls to automatically ensure we only deploy software that
has gone through our Software Development Lifecycle.  This can be implemented as
a gate in the pipeline, or as an admission control in the environment (ideally
both).

{{< figure src="/images/deployment-controls.svg" alt="Deployment Controls" >}}
