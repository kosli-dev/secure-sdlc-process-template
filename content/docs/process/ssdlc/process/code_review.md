---
title: Code Review
weight: 10
level: 1
tldr: Code review is performed on all software changes
rationale: Peer review is an essential mitigation against insider threats, as well as a means of improving knowledege sharing and quality.
risks: insider_threat
---

# {{% param "title" %}}
{{< area_head >}}

## Background
We use pull requests to document code reviews.  The pull request description should contain key information of the change, as well as any relevant information.  At a minimum, code reviews should be performed by someone capable of understanding the change and it’s associated risks.

Important considerations we make before approving a Pull Request:

- Security concerns: is this change secure?
- Quality: is this maintainable?
- Verification: Does this require manual testing? Has is been performed?

{{< figure src="/images/feature-branch-pr.svg" alt="Feature Branch Strategy" >}}

{{< hint warning >}}
### Code Review Anti-patterns

A common anti-pattern when using pull requests is waiting for review.  In an ideal situation, the lead time for review should approach 0.  If there is any delay on integration, it can lead to people batching larger and larger changes.  This causes larger pull requests, more delays, poorer code reviews, and ultimately more risks.

To avoid this, we recommend pair- or ensemble-programming: a practice where more than one person works together to complete tasks.  This way, as soon as one developer creates the pull request, another person can sign off immediately.

Note: the reviewer should not be the person who pushes the last commit on the branch.

{{< /hint >}}
