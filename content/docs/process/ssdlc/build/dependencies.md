---
title: Dependency Management
weight: 20
tldr: Every dependency is defined securely, managed, and auditable
rationale: Inputs to the build process can introduce security and quality issues, and as such must be defined, controlled, and transparent as part of the software development lifecycle.
level: 1
---

# {{% param "title" %}}
{{< area_head >}}

## Background



Key points:

* You must have control over what dependencies are packaged in your software
* All dependencies must comply with licensing requirements
* Must only use software with licences agreed by {{% param "company"  %}}

Dependencies can include docker base images, 3rd-party libraries, and other
source code.

![Dependencies](/images/dependencies.png)

During build, these inputs to the build package can be recorded as the software
bill-of-materials while recording
[binary provenance]({{< relref "/docs/process/ssdlc/build/binary_provenance" >}})

