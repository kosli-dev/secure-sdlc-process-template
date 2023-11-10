---
weight: 10
title: Why do you need a process?
---
# Who needs to define a software process?

Regulated software companies like banks, fintechs, healthcare providers, 
medical device manufacturers, etc. need to comply with government legislation 
and/or industry standards (IEC 62304, ISO26262, NIST, FDA, etc.) before they 
can take products to market and sell to customers. 

Many non-regulated companies also choose to opt-in to standards 
like SOC2 and ISO27001 to win the confidence of their customers.  

To achieve compliance with any of these regulations and standards 
involves defining a software delivery process, implementing it, 
and then proving that the process is being followed. 

This is why you need a software process. 

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

{{< figure src="/images/governance.svg" alt="Governance Framework" >}}

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



