---
title: "Deployment Approvals"
level: 1
weight: 40
tldr: Deployments are approved
rationale: To meet segregation of duties requirements, all deploymnents to production are approved by someone other than the person making the change
---

# {{% param "title" %}}
{{< area_head >}}

## Background

Segregations of duties is a common requirement in regulated or high security
development environment. Put plainly, it means that a developer cannot deploy
their own changes without approval from someone who both:

* Understands what is changing
* Accepts the risk of the change

{{< figure src="/images/deployment-approvals.svg" alt="Deployment Approvals" >}}

Deployment approval controls form a key role in the secure software development
lifecycle.  Its purpose is to ensure that risks around change are managed and
that change is an active decisions.

In highly sensitive software systems, more than one approver may be required.