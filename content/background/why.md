---
weight: 10
title: Why do you need a process?
---
# Why does {{% param "company"  %}} need a software process?

Regulated organizations such as banks, insurance companies, and payment
platforms obtain their license to operate from a government authority.   As a
critical element of the country's economy, and also to protect consumers, these
organizations are required by law to manage various **operational risks** in their
use of information technology.  For example, in Norway this regulating authority
is [Finanstilsynet](https://www.finanstilsynet.no/),
and the applicable law is the
[IKT forskrift](https://lovdata.no/dokument/SF/forskrift/2003-05-21-630).

In other countries the laws and regulations differ, but the principle is
internationally followed.
{{< figure src="/sdlctemplate/images/regulations.svg" alt="Governing Context" >}}

{{< hint info >}}
### Risk Management
Typical obligations in this framework include having processes around how IT
systems change, and managing the risks associated with changes.  Crucially, it
is expected that there are comprehensive records of these changes, and the risk
mitigations and internal controls performed as part of the changes.

This record of your changes should also contain evidence that your developers
are following your process and performing risk controls.
{{< /hint >}}

Essentially, we must:

1. *Define*: Have a defined process for software development
2. *Implement*: Actually follow this process in our daily work
3. *Prove*: Have the proof that we conform to the process during audit

{{< figure src="/sdlctemplate/images/governance.svg" alt="Governance Framework" >}}

## What should be in a SSDLC process?

Generally a process should define the activities and technologies used in the
development and maintenance of our software. In a regulated setting, the
rationale for given controls and processes should map to the risks identified
in governance.

- A risk register
- The areas of SSDCL
    - For each area:
      - A definition
      - Risks this area controls for
      - A rationale
      - Application rule (Mandatory, Optional)

{{< hint info >}}
## How should our SSDLC be documented?
It should be defined and available on an internal website and stored in a version controlled system such as git.
{{< /hint >}}

## Documenting Options and Exceptions

Exceptions and customizations should be defined in the exception register.



