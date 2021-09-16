# In-Solidarity IETF Configuration

This repo contains a [configuration file](.github/in-solidarity.yml) for
[in-solidarity-bot](https://github.com/apps/in-solidarity) that flags some of
the terms in [the NIST Technical Series Publications Author
Instructions](https://www.nist.gov/nist-research-library/nist-technical-series-publications-author-instructions#inclusive)
and [the IETF's list of problematic
terminology](https://github.com/ietf/terminology).

## Usage

If you want to use this configuration, you have two choices: you can enable it
for an entire GitHub organization and all its repos, or you can enable it for an
individual repo.

In either case, you will of course need to install and enable the
[in-solidarity-bot](https://github.com/apps/in-solidarity) for your repo or
organization, so do that first by [clicking "Configure" on this
page](https://github.com/apps/in-solidarity) and then enabling the bot
accordingly.

### Enabling for a GitHub Organization or User

After enabling [in-solidarity-bot](https://github.com/apps/in-solidarity), in
order to enable the configuration in this repo for your entire GitHub user
account or organization, simply

1. **fork** this repo into your organization or user account
2. **rename** the forked repo to `.github`

If you already have a `.github` repo in your organization or user account,
<!--
follow the steps in the next section instead, creating a
`.github/in-solidarity.yml` file in your existing `.github` repo.
-->
you need to unfortunately enable the configuration for each repository,
as described in the next section. (If someone knows a way for enabling this
per-organization, please contact me!)

### Enabling for a Single Repository

After enabling [in-solidarity-bot](https://github.com/apps/in-solidarity), in
order to enable the configuration in this repo for a single repo, execute these
shell commands at the top-level directory of the target repo:

``` shell
mkdir .github
echo "_extends: NTAP/isb-ietf-config" > .github/in-solidarity.yml
git add .github/in-solidarity.yml
git commit -m "Add in-solidarity-bot config"
```

This will create and commit a `.github/in-solidarity.yml` file that uses the
configuration provided in this repo.

## Suggesting New Terms

[These regular expression-based rules](.github/in-solidarity.yml) control which
terms will be flagged at which severity level, and also contains lists of
alternative terms that will be suggested.

Please open a pull request against this file to suggest new terms to be added to
the configuration.
