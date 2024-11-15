---
title: Service ownership
level: 1
weight: 50
control_code: KVC5
tldr: All services running in our environments have registered ownership
rationale: In a diverse software landscape it is essential everyone knows who
  is responsible for maintaince and support
areas: 
 - process
---
# {{% param "title" %}}
{{< area_head >}}

## Background

In any governance system, risks are managed by controls. But humans are ultimately responsible.In this context there are many reasons to keep a register of service ownership in diverse software
landscapes:

* **Knowlege**: Who knows how this is supposed to work?  How can I get help with this system?
* **Incident**: Alerts are firing for a service, who do I contact?  What has changed lately?
* **Audit**: who is reponsible that the SDLC is followed for this service?

{{< figure src="/images/secrets-management.svg" alt="Change Records" >}}

## How we implement this control

At this stage, as we have a relatively simple system and a single tech team, simply recording the services in [Kosli's environment monitoring]({{< ref "workload_monitoring.md" >}}) meets this need.

