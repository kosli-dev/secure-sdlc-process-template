---
title: Immutable Toolchain
weight: 20
tldr: Build environments must be defined securely and auditable
---
# {{% param "title" %}}
{{< area_head >}}

The Build security levels defined in the [slsa specification](https://slsa.dev/spec/v0.1/requirements#scripted-build) are as follows:

1. Scripted
1. Ran in a controlled build service
1. Defined as code (CI definition)
1. Ephemeral environment
1. Isolated
1. Parameterless
1. Hermetic
1. Reproducible

