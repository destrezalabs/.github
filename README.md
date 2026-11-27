# .github

Organization-level files for Destreza Labs.

This repository must stay public. GitHub applies the default community health files below to every
repository in the organization only when they come from a public `.github` repository.

| Path | What it does |
|---|---|
| `SECURITY.md` | Default security policy |
| `.github/ISSUE_TEMPLATE/` | Default issue forms: feature, task, bug; blank issues off |
| `.github/pull_request_template.md` | Default pull request template |
| `workflow-templates/` | Starter workflows offered in the Actions tab; they call the shared reusable workflows |
| `profile/README.md` | The public organization profile |

CI logic is not hosted here. The starter workflows call the reusable workflows in
`kibanyadev/.github`, pinned by commit SHA with the release tag in a comment.
