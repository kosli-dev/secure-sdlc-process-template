---
title: Runtime Workload Monitoring
level: 1
weight: 50
control_code: KCC5
tldr: Workloads are monitored to alert if any non-compliant or unauthorized change is discovered
rationale: Real-time closed-loop compliance monitoring is a constant vigil against threats
areas: 
 - change
---

# {{% param "title" %}}
{{< area_head >}}

## Background

Ensuring that risks are controlled in the value stream is the first level of
software process compliance.  Beyond this, it is important to have a monitoring
process in place to ensure that unknown or non-compliant workloads are identified
in production.

{{< figure src="/images/workload-monitoring.svg" alt="Workload Monitoring" >}}

## How we implement this control

* A full forensic history of all container runtimes, lambda functions and s3 buckets are recorded using [Kosli environments](https://www.kosli.com/blog/kosli-a-flight-data-recorder-for-your-runtime-environments/) and can be found here: https://app.kosli.com/kosli/environments/
* Unauthorized or non-compliant workloads are recorded and create alerts in our slack channels

