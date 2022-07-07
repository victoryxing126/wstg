# Workflows Documentation

## `build-pdf.yml`

For building PDFs at release.

- Trigger: Tag applied to repository. Manual (`workflow_dispatch`), GitHub web UI.
- See: `/.github/pdf/` in the root of the repository.

## `dummy.yml`

Utility action so that PRs without Markdown files can pass the branch protection rules. `lint` is required per the branch protection rules. If a PR contains no Markdown files (e.g. only an image or YAML that isn't linted) the dummy runs and passes the branch protection requirement.

- Trigger: Pull Requests.

## `md-link-check.yml`

Checks Pull Requests for broken links.

- Trigger: Pull Requests.
- Config File: `markdown-link-check-config.json`

## `md-lint-check.yml`

Checks Markdown files and flags style or syntax issues.

- Trigger: Pull Requests.
- Config File: `.markdownlint.json`

## `md-textlint-check.yml`

Checks Markdown files for spelling style and typo issues.

- Trigger: Pull Requests.
- Config File: `.textlintrc`

## `www_latest_update.yml`

Publishes the latest web content using the @wstgbot account to `OWASP/www-project-web-security-testing-guide`.

- Trigger: Push.
- See: `/.github/www/latest/` in the root of the repository.

## `www_stable_update.yml`

Publishes stable and versioned web content using the @wstgbot account to `OWASP/www-project-web-security-testing-guide`.

- Trigger: Tag applied to repository (format `v*`).
- See: `/.github/www/` in the root of the repository.
