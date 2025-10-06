---
weight: 30
title: DevOps Compliance Culture
---

# DevOps Compliance Culture

> TLDR: DevOps teams who understand and conform to process with automation support outperform teams with external approvals and compliance managers.

The way we build and deliver software has changed significantly over the years.  In the past, we would build systems on large, custom managed hardware.  Organizations were siloed by specialty, with different departments for analysis, development, quality assurance, and operations.  Software was delivered in releases, once a year, or once a quarter even.  Change was rare, risky, and large.

{{< figure src="/images/changes-over-time.svg" alt="Software Landscape" >}}

Over time, we have favoured smaller services-oriented architectures and independently deployable systems.  This allowed for more dynamic and resillient designs, and to leverage Conway's Law to organize our teams around these services.

This trend continues, with the rising adoption of serverless features and functions-as-a-service available in cloud providers.

## Who is responsible for compliance?

Traditionally, it was the IT department who were responsible for changing IT systems, and the volume of changes was relatively low.  This also meant that the responsibility of meeting these regulatory obligations rested with the IT department.

{{< figure src="/images/value-stream.svg" alt="Value Stream" >}}

## The Compliance Bottleneck
Conventional Change Management approaches in regulated industries have been IT-led, such as [ITIL practices](https://en.wikipedia.org/wiki/ITIL), change tickets, [Change Advisory Board meetings](https://en.wikipedia.org/wiki/Change-advisory_board), and scheduled changes.  However, these processes were designed for infrequent changes and causes delays and batching changes.  Somewhat counter-intuitively, these practices designed to reduce risk actually lead to increased delivery risks.

> "External approvals were negatively correlated with lead time, deployment frequency, and restore time, and had no correlation with change fail rate. In short, approval by an external body (such as a manager or CAB) simply doesn't work to increase the stability of production systems, measured by the time to restore service and change fail rate. However, it certainly slows things down. It is, in fact, worse than having no change approval process at all" [^20]

{{< hint info >}}
To learn more about this, look into the findings from UK's Financial Conduct Authority 👉 [here](https://www.kosli.com/blog/what-the-fca-found-when-analysing-1-million-production-changes/)
{{< /hint >}}

## Building a DevOps Culture around Compliance

Modern technology organizations are organized differently.  The traditional separation between Software Development, Quality Assurance, and IT Operations has been replaced by cross-functional devops teams responsible for the entire value stream of software systems.  This new DevOps approach allows organizations to reduce handovers, increase collaboration, and ultimately deliver more innovation.

{{< figure src="/images/collective-ownership.svg" alt="Collective Ownership" >}}

As organizations change, the supporting technology approaches also change.  Companies are adopting metered cloud infrastructure as a service, automated build, test and security tooling.  With the support of this automated devops delivery, high performing teams can deliver changes 973 times[^1] more frequently than traditional teams.
If we need to be compliant, but external approvals and management don't work, what should we do?


## Continuous Compliance

This vast increase in the number of changes needs new and better approaches to change management and software process compliance.  To support the efforts of devops teams, we need to move away **from manual gated checks** towards **continuous automated checks**.

| Need | Traditional Compliance | Continuous Compliance |
| ----------- | ----------- | ----------- |
| Process conformance | Checklists | Risk controls as code |
| Change Managment | Change Tickets | Self documenting changes |
| Governance | Audits | Compliance monitoring |

In this way, we can not only achieve more flow in our work, but actually get better compliance.

{{< hint info >}}
We have seen in practice that adoption of continuous compliance methodology lead to the similar benefits that test automation brings.

Adopting test automation the need for testers does not go away, merely the monotonous repeatitive work.  This frees testers to work at higher-level exploratory testing.

In the same way, Continuous Compliance does not mean the end of compliance work, but rather enables compliance officers to work on higher value compliance investigation.
{{< /hint >}}


## Conclusions: the Advantage of DevOps Compliance Cultures

The devops principles around culture, automation, lean, measurment and sharing can help teams increase compliance activities while reducing delays and waste.  Overall the benefits from adopting a DevOps Compliance Culture are:

* **Culture**: creates agency for teams to lead risk management responsibilities
* **Automation**: drives higher compliance conformance and reduces waste
* **Lean**: results in continuous improvement in risk control posture
* **Measurement**: ensures compliance becomes data-driven
* **Sharing**: makes compliance work visible to empower compliance and security functions


[^1]: https://cloud.google.com/devops/state-of-devops
[^20]: Forsgren PhD, Nicole. Accelerate: The Science of Lean Software and DevOps: Building and Scaling High Performing Technology Organizations . IT Revolution Press. Kindle Edition.
