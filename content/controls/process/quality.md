---
title: Quality Assurance
level: 1
weight: 20
tldr: Functionality of software is assured prior to production
rationale: Every change has the potential to introduce regressions in functionality.  By testing our software prior to deployment we manage the risk of production issues.
areas: 
 - process
---

# {{% param "title" %}}
{{< area_head >}}

## Background

If it matters that a software system functions according to expectations, we must test and qualify our software prior to production. The level of testing and qualification should correspond to the risk appetite for a particular system.  Testing can be either manual or automated (however we recommend automated approaches such as unit testing).  Regardless of the approach, the testing approach must be systematic and test results documented.

{{< hint warning >}}
The benefits of automated approaches to regression testing include:

* Less manual work
* More consistent testing
* Faster lead times
* Improved knowledge sharing
* Automated test results documentation

{{< /hint >}}

## How we implement this control

For any software delivered to customers, or with potential to impact customer data, we will test all software prior to deployment/release.  Our main testing method will favor automated tests, both on the unit and integration level.  (As of this time, our server software has over 95% branch coverage).

* We perform automated testing as part of our CI/CD pipelines
* We record the automated test results against the code and artifacts in our [Kosli Flows](https://app.kosli.com/kosli/flows/)
* We control that tests are passing and test results are stored prior to deployment

In addition, we can perform these controls which are optional but good practice:

* We have a test coverage ratchet that fails if a coverage goal is not met
* This ratchet fails the pipeline
* A manual intervention is required to lower the coverage goal