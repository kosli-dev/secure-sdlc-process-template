---
title: Controlled Build Environment
level: 3
weight: 30
control_code: KBC3
areas: 
 - build
tldr: Build environments must be defined as code, ephemeral, and auditable
rationale: A secure build environment is the foundation for a mitigating software supply chain attacks.  Build environments defined as code protect against interference that can happen in the build and distribution processes.
---
# {{% param "title" %}}
{{< area_head >}}

## Background
Builds that are scripted, ran in an ephemeral and controlled build environment
are more resilient against supply chain attacks.  If at all possible, we
recommend teams use immutable docker images to define the build environment.
This enables auditing of the build environment, as well as security scanning and
version control.

{{< figure src="/images/defined-toolchain.svg" alt="Toolchain" >}}

{{< hint info >}}
You can learn more about build security levels defined in the [slsa specification](https://slsa.dev/spec/v0.1/requirements#scripted-build).
{{< /hint >}}

## How we implement this control

* Our officical builds occur in Github pipelines defined as code
* Each step runs in an immutable container
* Each build fingerprint is stored using [Binary Provenance]({{< ref "binary_provenance.md" >}})