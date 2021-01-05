# sitepreview

![GitHub repo size](https://img.shields.io/github/repo-size/seismo-learn/sitepreview)
![CI](https://github.com/seismo-learn/sitepreview/workflows/CI/badge.svg)

The `gh-pages` branch of this repository hosts the documentation from PRs
of other repositories, so that we can preview the changes in PRs.

## How does it work

PRs of other repositories can run workflow, generate the documentation, and
push the documentation to the `gh-pages` branch of this repository.

The URL scheme is:

    https://seismo-learn.org/sitepreview/seismo-learn/<repository_name>/<PR_branch_name>

See https://github.com/seismo-learn/software/pull/29 for the workflow changes.

## Cleanup

The [workflow](.github/workflows/cleanup.yaml) runs daily to:

1. Delete the documentation if the corresponding branch was deleted
2. Generate an index file, which lists all current documentations
3. Squash all commits into one commit to avoid increasing repository size
