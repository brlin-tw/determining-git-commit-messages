---
name: determining-git-commit-messages
description: Provide guidelines on how to determine appropriate git commit messages that are compliant with project standards. Should be used when generating, modifying, or reviewing git commit messages.
---

# The determining-git-commit-messages agent skill

Provide guidelines on how to determine appropriate git commit messages that are compliant with project standards. It should be used when generating, modifying, or reviewing git commit messages.

## Always follow existing style

Always read the previous commit messages of the staged files and mimic the style and format used in those messages.

If there are no previous commit messages for the staged files, refer to previous commit messages in similar files or modules within the same project to maintain consistency.

## When no existing commit style found

Only use the following rules if there're no existing commits for reference:

* Use the [Conventional Commits specification](https://www.conventionalcommits.org/).
* Use the human's identity for Developer Certificate of Origin (DCO) sign-off.
* Follow [Attribution — AI Coding Assistants — The Linux Kernel documentation](https://docs.kernel.org/process/coding-assistants.html#attribution) for AI tooling disclosure.
