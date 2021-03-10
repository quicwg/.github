This repo contains a [configuration file](.github/in-solidarity.yml) for
[in-solidarity-bot](https://github.com/apps/in-solidarity) that flags
the terms in [the IETF's list of problematic
terminology](https://github.com/ietf/terminology).

If you want to use this with your repository, you can do this at the top of your
repo:

``` shell
mkdir .github
git submodule add https://github.com/NTAP/isb-ietf-config.git .github/isb-ietf-config
ln -s isb-ietf-config/.github/in-solidarity.yml .github/
git add .github/in-solidarity.yml
git commit -m "Add in-solidarity-bot config"
```

You can also enable this for all repos in your org by  forking this repo into
a `.github` repo inside your org.

You will of course also need to install the
[in-solidarity-bot](https://github.com/apps/in-solidarity)
for your repo or organization.
