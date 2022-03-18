---
title: Code Review
weight: 10
level: 1
tldr: Code review is performed on all software changes
---

# {{% param "title" %}}
{{< area_head >}}


We use pull requests to document the changes to code.  It should contain a description of the change, as well as any relevant information.  At a minimum, code reviews should be performed by someone capable of understanding the change and it’s associated risks.

Important considerations we make before approving a Pull Request:

- Security concerns: is this change secure?
- Quality: is this maintainable?
- Verification: Does this require manual testing? Has is been performed?

Risk of going into production

