---
title: Defined Toolchain
level: 3
weight: 20
tldr: Build environments must be defined securely and auditable
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

