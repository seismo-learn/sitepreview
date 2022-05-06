# sitepreview

![GitHub repo size](https://img.shields.io/github/repo-size/seismo-learn/sitepreview)
[![Clean up](https://github.com/seismo-learn/sitepreview/actions/workflows/cleanup.yaml/badge.svg)](https://github.com/seismo-learn/sitepreview/actions/workflows/cleanup.yaml)

The `gh-pages` branch of this repository hosts the documentation from PRs
of other repositories, so that we can preview the changes in PRs.

## How it works

The [`preview-pr.yml`](https://github.com/seismo-learn/seismology101/blob/main/.github/workflows/preview-pr.yml)
workflow is triggered in PRs. It builds and pushes the documentation to the
`gh-pages` branch of this repository, and creates/updates a comment
with the preview URL link.

The URL scheme is:

    https://seismo-learn.org/sitepreview/seismo-learn/<repository_name>/<PR_branch_name>

## Cleanup

The [cleanup workflow](.github/workflows/cleanup.yaml) runs daily to:

1. Delete the documentation if the corresponding branch was already deleted
2. Generate an index file, which lists all documentations of current open PRs
3. Squash all commits into one commit to avoid increasing repository size
