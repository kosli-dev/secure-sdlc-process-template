---
title: Dependency Management
weight: 20
areas: 
 - build
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

{{< figure src="/images/dependency-management.svg" alt="Dependency Management" >}}


During build, these inputs to the build package can be recorded as the software
bill-of-materials while recording
[binary provenance]({{< relref "/process/ssdlc/build/binary_provenance" >}})

## How we implement this control

We define these dependencies in the source code, at the application level and if relevent, at the Docker image level.

| Application | Dependencies |
| ----------- | ------------ |
| CLI | [Golang Dependencies](https://github.com/kosli-dev/cli/blob/main/go.mod) |
| Server | [Python Dependencies](https://github.com/kosli-dev/server/blob/master/src/requirements.txt) <br/> [Docker Dependencies](https://github.com/kosli-dev/server/blob/master/Dockerfile) |
| Slack Application | [Python Dependencies](https://github.com/kosli-dev/slack-auth-app/blob/main/src/requirements.txt) <br/> [Docker Dependencies](https://github.com/kosli-dev/slack-auth-app/blob/main/Dockerfile) |