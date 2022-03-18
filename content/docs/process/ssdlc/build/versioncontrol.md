---
title: Version Control
weight: 1
level: 1
tldr: Every change to the source is tracked in a version control system
---
# {{% param "title" %}}
{{< area_head >}}

We use git to manage versioning for software development source code.  For repository hosting and user management we use Atlassian Bitbucket.


## Branching Strategies

Every service will follow one of the following branching strategies:

* Feature Branch + Pull Request
* Production Branches

These are described below.

### Feature Branch + Pull Request

This branching strategy uses a combination of feature branches with pull requests.

![Feature Branch Strategy](/images/feature-branch-pr-strategy.png)

* Master branch is protected
* Pull requests must be approved before merge to master.
* We use pull requests to enforce and document our code review process.  You can read more about it here: Code Review Process
* Pull request merges will create merge or squash commits. (no fast-forward)
* For repositories that contain production code, we will utilize a production tracking branch, which is updated by the deployment pipeline stage with ff-only merges.

On deployment to production, we update the production branch to point to the related commit.  This enables development team to have visibility on production from git. The merge looks like this:

![Feature Branch Strategy](/images/production-tracking-branch.png)

Merges to master should either be merge commits or squash commits... i.e. no fast-forward merges.  This allows us to atomically back out merges should we need to.


### Production Deployment Branch

The Production Deployment branch is an alternative to the feature-branch/pull-request strategy.

This allows a model similar to trunk-based-development, where code reviews are implemented in the merge to production.

* Production branch is protected
* Pull requests must be approved before merge to production.
* We use pull requests to enforce and document our code review process.  You can read more about it here: Code Review Process
* Pull request merges will fast-forward. This means the production branch will always “point” to a commit on the master branch

### Protected Deployment Branches

To ensure compliance to the code review process, we protect the branch we deploy from (master or production) with the following requirements:

* Merges require at least one approval (two if the strategy is Production Deployment Branch)
* Builds and tests run successfully
* No unresolved merge checks

