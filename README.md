This repo contains a [configuration file](.github/in-solidarity.yml) for
[in-solidarity-bot](https://github.com/apps/in-solidarity) that flags some of
the terms in [the NIST Technical Series Publications Author
Instructions](https://www.nist.gov/nist-research-library/nist-technical-series-publications-author-instructions#inclusive)
and [the IETF's list of problematic
terminology](https://github.com/ietf/terminology).

If you want to use this with your repository, you can do this at the top-level
directory of your repo:

``` shell
mkdir .github
echo "_extends: NTAP/isb-ietf-config" > .github/in-solidarity.yml
git add .github/in-solidarity.yml
git commit -m "Add in-solidarity-bot config"
```

You can also enable this for all repos in your org by simply forking this repo
into a `.github` repo inside your org.

You will of course also need to install and enable the
[in-solidarity-bot](https://github.com/apps/in-solidarity)
for your repo or organization.
