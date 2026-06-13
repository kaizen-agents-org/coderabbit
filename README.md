# Kaizen Agents CodeRabbit Configuration

This repository stores the organization-wide CodeRabbit configuration for
`kaizen-agents-org`.

CodeRabbit applies `.coderabbit.yaml` from this repository to repositories that
do not define their own `.coderabbit.yaml`.

## Required Setup

1. Install the CodeRabbit GitHub App for `kaizen-agents-org`.
2. Include the `kaizen-agents-org/coderabbit` repository in the installation.
3. Include every repository that should receive CodeRabbit reviews:
   - `builder-agent`
   - `kaizen-loop`
   - `verifier`
   - `.github`
4. Open a pull request in a configured repository and confirm CodeRabbit reports
   `Repository: coderabbit/.coderabbit.yaml` as the configuration source.

## Review Behavior

- CodeRabbit automatically reviews non-draft pull requests targeting each
  repository's default branch.
- Incremental reviews run on new pushes.
- Draft PRs and PRs titled `WIP`, `DO NOT MERGE`, or `[skip review]` are skipped.
- `dependabot[bot]` and `renovate[bot]` PRs are skipped.
- CodeRabbit can request changes for blocking review findings.

Manual review commands:

```md
@coderabbitai review
@coderabbitai full review
```

## Codex Review Setup

Codex code review is configured in ChatGPT, not in this repository:

1. Set up Codex cloud for each repository.
2. Open <https://chatgpt.com/codex/settings/code-review>.
3. Turn on Code review for each repository.
4. Optionally turn on Automatic reviews.

Manual review command:

```md
@codex review
```

Codex reads `AGENTS.md` review guidance in each repository when reviewing pull
requests.
