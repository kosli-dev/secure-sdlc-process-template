---
weight: 30
title: DevOps Culture and Process
---

# DevOps Culture and Process

The way we build and deliver software has change significantly over the years.  In the past, we would build systems on large, custom managed hardware.  Organizations were siloed by specialty, with different departments for analysis, development, quality assurance, and operations.  Software was delivered in releases, once a year, or once a quarter even.  Change was rare, risky, and large.

![Software Landscape](/images/landscape.png)

Over time, we have favoured smaller services-oriented architectures and independently deployable systems.  This allowed for more dynamic and resillient designs, and to leverage Conway's Law to organize our teams around these services.

This trend continues, with the adoption of the latest serverless and functions-as-a-service available in cloud providers.

Traditionally, it was the IT department who were responsible for changing IT systems, and the volume of changes was relatively low.  This also meant that the responsibility of meeting these regulatory obligations rested with the IT department.  The common implementation of this was often using [ITIL practices](https://en.wikipedia.org/wiki/ITIL), such as change tickets, Change Advisory Board meetings, and schedules.

Modern technology organizations are organized differently.  The traditional separation between Software Development, Quality Assurance, and IT Operations has been replaced by cross-functional devops teams responsible for the entire value stream of software systems.  This new DevOps approach allows organizations to reduce handovers, increase collaboration, and ultimately deliver more innovation.

As these organizations change, the supporting technology approaches also change.  Companies are adopting metered cloud infrastructure as a service, automated build, test and security tooling.  With the support of this automated devops delivery, high performing teams can deliver changes 973 times[^1] more frequently than traditional teams.

This vast increase in the number of changes needs new and better approaches to change management and software process compliance.

[^1]: https://cloud.google.com/devops/state-of-devops