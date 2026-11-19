# repo-template

The smallest repository that passes Datum's required CI check from its first commit.

Create a repository from this template when it has to pass `ci / Build and test` but needs no service skeleton. For a new Go service, use [service-template](https://github.com/datum-cloud/service-template) instead.

It holds four files:

- `.github/workflows/ci.yaml` calls the shared `ci-basic` workflow. That workflow finds Go, Node and Python projects and a Dockerfile, and builds and tests what it finds. Until the repository has any of those, the `run` step is all that runs. Delete the `run` line once there is real code to check.
- `.github/CODEOWNERS` names this template's owner. The github-org program in datum-cloud/infra replaces it, in the apply that creates a repository, with one naming the teams declared as that repository's code owners.
- `renovate.json` keeps the `ci-basic` pin and later dependencies current.
- This README. Replace it.
