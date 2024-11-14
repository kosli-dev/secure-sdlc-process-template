---
title: Infrastructure and Configuration Management
level: 1
weight: 50
tldr: Infrastructure and Configurations are defined "as code" and applied through automation
rationale: Software defined cloud infrastructure allows auditability, reproducibility and drift detection
areas: 
 - build
---

# {{% param "title" %}}
{{< area_head >}}

## Background
Infrastructure setup, configuration and evolution must be auditable, secure and reproducible.  To ensure this we define our cloud environments as code and use automation tools to automatically roll out changes.

## How we implement this control

* To ensure this we define all our production and test infrastructure using code.  Changes are rolled out via CI pipelines in {{% param "gitProvider"  %}}
* We use the appropriate for the type and level of the change  (e.g. Terraform for infrastructure, Docker for application Runtimes)
* All documentation around our infrastructure, security approaches and automation is maintained and up-to-date in our [Knowledge Base](https://github.com/kosli-dev/knowledge-base)