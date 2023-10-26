---
title: Version Control
weight: 1
level: 1
tldr: Every change to the source is tracked in a version control system
rationale: Version control allows us to track and manage changes to our software code.  As a traceability system, it provides a means to understand how our software changes, who changes it, and why it was changed.
---
# {{% param "title" %}}
{{< area_head >}}

## Background
We use {{< param "vcs"  >}} to manage versioning for software development source code.  For repository hosting and user management we use {{< param "vcsHost"  >}}.


## Branching Strategies

Every service will follow one of the following branching strategies:

1. Feature Branch + Pull Request, or:
2. Production Branches

These are described below.

### 1. Feature Branch + Pull Request

This branching strategy uses a combination of feature branches with pull requests.

{{< figure src="/images/feature-branch-pr.svg" alt="Feature Branch Strategy" >}}

* Main branch is protected
* Pull requests must be approved before merge to the main branch.
* We use pull requests to enforce and document our code review process.  You can read more about it here: [Code Review Process]({{< relref "/process/ssdlc/process/code_review" >}})
* Pull request merges should create merge or squash commits. (no fast-forward)


Merges to the main should either be merge commits or squash commits... i.e. no fast-forward merges.  This allows us to atomically back out merges should we need to.


### 2. Production Deployment Branch

The Production Deployment branch is an alternative to the feature-branch/pull-request strategy.

This allows a model similar to trunk-based-development, where code reviews are implemented in the merge to production.

* Production branch is protected
* Pull requests must be approved before merge to production.
* We use pull requests to enforce and document our code review process.  You can read more about it here: Code Review Process
* Pull request merges will fast-forward. This means the production branch will always “point” to a commit on the main branch

### Protected Deployment Branches

To ensure compliance to the code review process, we protect the branch we deploy from (main or production) with the following requirements:

* Merges require at least one approval (two if the strategy is Production Deployment Branch)
* Builds and tests run successfully
* No unresolved merge checks

