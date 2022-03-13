---
title: Artifact Binary Provenance
weight: 1
sdlc_area: Artifact Binary Provenance
tldr: Every software running production has known provenance
risks:
 - supply-chain

---

# {{% param "title" %}}
{{< area_head >}}

In high security environments we need a tamper-proof identity scheme. In plain talk, if the software changes we want it to have a different identity.

It must be impossible to qualify one artifact and deploy a different artifact.

Luckily, this is a solved problem in computer science. The solution is Content Addressable Storage.

How this works is really simple. Instead of using a label to define software identity, you use the cryptographic hash of the software itself.

This means that if a single byte in the software changes it will have a different identity.

![Binary Provenance](/images/binary-provenance.svg)

## What to store in the system of record?

- The SHA256 of the artifact (docker image, zip file, ...)
- A human readable name
- The git commit that produced it
- The git repository state (clean, unstaged files, ...)
- A url to the build log
- The build environment information
- The software bill of materials

## Alternative identification of artifacts

While Does this mean SemVer is dead? That you shouldn’t use git SHAs to identify your software? Not at all!

These are very useful ways for humans to navigate identity through version control and CI systems. However, since they are fallible, we still need the primary key of identity to be the content-addressable storage, linked to the labels. Labels are for humans and SHAs are for machines.