# Tailored AI website 
[here](https://tai-src.github.io/)


## Maintenance notes

Generally, to add a new page, add an md file in the [docs folder](tai/docs/). For it to be included into the navigation, it also needs to be added to [mkdocs.yml](tai/mkdocs.yml). However, there is a [script](tai/main.py) that can be set up to create an index of all files in a folder ([example](tai/docs/projects/index.md)) if they are not all supposed to be available through the nav menu.

### Deployment
[![Publish docs via GitHub Pages](https://github.com/TAI-src/tai-src.github.io/actions/workflows/deploy_mkdocs.yml/badge.svg)](https://github.com/TAI-src/tai-src.github.io/actions/workflows/deploy_mkdocs.yml)

First, an action runs that builds the mkdocs and puts the static files that result from this into a separate branch called 'gh-pages'.

[![pages-build-deployment](https://github.com/TAI-src/tai-src.github.io/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/TAI-src/tai-src.github.io/actions/workflows/pages/pages-build-deployment)

Afterwards, the default GH Pages action (set up in repository setting) deploys the static files from that branch.
