# sitepreview

The `gh-pages` branch of this repository hosts the documentation from PRs
of other repositories, so that we can preview the changes in PRs.

## How does it work

PRs of other repositories can run workflow, generate the documentation, and
push the documentation to the `gh-pages` branch of this repository.

The URL scheme is:

	https://seismo-learn.org/sitepreview/seismo-learn/<repository_name>/<PR_branch_name>

See https://github.com/seismo-learn/software/pull/29 for the workflow changes.
