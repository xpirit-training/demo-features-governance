# Demo of Legitify by Legit-Labs

Repository to demonstrate use of [Legit-Labs Legitify](https://github.com/legit-labs/legitify) for repository governance.

## Workflows

Legitify provides a GitHub action that can be used. The action needs authentication through a [PAT](#pat). As this is not neccessarily best practice an approach using a [GitHub App](#github-app) is investigated as well. Please see below to get further details about the two methods.

### PAT

This is the main and working workflow to scan this repository according to Legitify's default policies. The execution is manual as this is a demo. In a productive setting this scan should be scheduled on a daily or weekly basis.

The workflow creates an issue on success or failure to notify about the results. The issues are created  from templates located at `.github/templates`. The templates contain placeholder that are replaced in the workflow run using [`jinja2`](https://jinja.palletsprojects.com/en/3.0.x/).

### GitHub App

The target perform the scan through a GitHub app to avoid using a PAT. This does not work yet and needs to be further investigated.

## Policies

Legitify check for a number policies that are documented in [Legitify's docs](https://legitify.dev/github/).
