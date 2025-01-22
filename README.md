# United Security Providers Documentations 

Welcome to the United Security Providers Documentations page. This repository contains the scripts and content to provide
the documentation overview site:

* https://docs.united-security-providers.ch/

## Requirements

- `docker`
- (`mkdocs` & `mkdocs-material`) to generate the website and deploy it to GitHub pages.

### mkdocs notes

* It's recommended to use the docker image to avoid system dependencies:
https://squidfunk.github.io/mkdocs-material/getting-started/#with-docker


```
$ docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material --version
mkdocs, version 1.6.1 from /usr/local/lib/python3.11/site-packages/mkdocs (Python 3.11)
```

## Generate site locally

```
$ docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material build
```

## Test site locally

```
$ docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
```

This will make it available locally (URL visible in output on the shell, typically http://127.0.0.1:8000/).

## Generate site and publish it via GitHub

To generate the site and deploy it to GitHub pages, run:

```
$ docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material gh-deploy --force
```

