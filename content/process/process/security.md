---
title: Security Vulnerability Scanning
level: 1
weight: 30
tldr: Software is scanned for security vulnerabilities prior to deployment
rationale: Many common security vulnerabilities can be detected with automated tools.  By implementing tools for dependency scanning, SAST, and DAST in the pipeline we can reduce the attack surface of our software
areas: 
 - process
---

# {{% param "title" %}}
{{< area_head >}}

## Background

<img src="/images/magnifyingglass.png" width="200"/>

Vulnerability scanning is the automated process of proactively identifying
software vulnerabilities in software.  Many common security attacks such as
vulnerable components and insecure coding techniques can be prevented by
integrating these tools in your devops, and acting in a timely manner on
issues found.

At minimum, we recommend dependency scans in the pipelines.  More advanced tools
such as Synk can help identify vulnerabilities post deployment, and help with
remedial actions.

* Implement security scanning in the pipeline
* Act in a timely manner to security issues
* Consider security concerns in code reviews and software design

## How we implement this control

* We use [snyk](https://snyk.io/) to scan code and dependencies in our CI/CD pipelines
* We record snyk scans in Kosli and control/monitor that no artifact with missing and/or failed snyk scans run in production

While not mandatory for our process, we additionally:

* Run continuous nightly snyk scans on containers in production in case new vulnerabilities are found in running assets