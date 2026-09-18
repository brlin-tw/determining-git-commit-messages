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
* Follow [Attribution — AI Coding Assistants — The Linux Kernel documentation](https://docs.kernel.org/process/coding-assistants.html#attribution) for AI tooling disclosure:

    > ## Attribution
    >
    > When AI tools contribute to kernel development, proper attribution helps track the evolving role of AI in the development process. Contributions should include an Assisted-by tag in the following format:
    >
    > Assisted-by: AGENT\_NAME:MODEL\_VERSION \[TOOL1\] \[TOOL2\]
    >
    > Where:
    >
    > * `AGENT_NAME` is the name of the AI tool or framework
    > * `MODEL_VERSION` is the specific model version used
    > * `[TOOL1] [TOOL2]` are optional specialized analysis tools used (e.g., coccinelle, sparse, smatch, clang-tidy)
    >  
    >
    > Basic development tools (git, gcc, make, editors) should not be listed.
    >
    > Example:
    >
    > Assisted-by: Claude:claude-3-opus coccinelle sparse

  `MODEL_VERSION` should include the full model identifier (not just the family name, not including reasoning effort, in dash-separated lowercase letters, digits, and dots), example:

    + `claude-sonnet-5`
    + `gemini-3.8-flash`
    + `gpt-5.6-sol`

  If the harness doesn't provide it ask the human first.

  The `Assisted-by` commit trailer should appear before any other trailers of the commit message.
