# .github

Organization-level files for Destreza Labs.

This repository must stay public. GitHub applies the default community health files below to every
repository in the organization only when they come from a public `.github` repository.

| Path | What it does |
|---|---|
| `SECURITY.md` | Default security policy |
| `.github/ISSUE_TEMPLATE/` | Default issue forms: feature, task, bug; blank issues off |
| `.github/pull_request_template.md` | Default pull request template |
| `.github/workflows/reusable-actionlint.yml` | Reusable: actionlint schema check of a repo's workflows |
| `.github/workflows/reusable-zizmor.yml` | Reusable: zizmor security audit of a repo's workflows (`version` input) |
| `.github/workflows/reusable-site-ci.yml` | Reusable: pnpm install and `verify` scripts, optional Playwright (inputs: `node-version-file`, `working-directory`, `scripts`, `playwright-filter`, `traces-path`, `artifact-name`, `timeout-minutes`) |
| `.github/workflows/ci-actionlint.yml`, `ci-zizmor.yml` | This repo's own lint, calling the reusable ones locally |
| `workflow-templates/` | Starter workflows offered in the Actions tab; they call the reusable workflows here (re-pinned to this repo's v1.0.0 in a follow-up) |
| `profile/README.md` | The public organization profile |

The reusable workflows live here. Callers in other `destrezalabs` repos pin them by commit SHA with the
release tag in a comment (`@<sha> # v1.0.0`), never `# main`. The repo must stay public so private
repos can call them, and the org Actions policy must allow actions from this repository.
