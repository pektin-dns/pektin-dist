# Mirror to GitHub and GitLab

git mirror and docker build

```yml
include:
    - project: pektin/pektin-dist
      ref: main
      file:
          - scripts/docker-build-and-publish.yml

image: alpine

variables:
    IMAGE_NAME:

stages:
    - docker-build-and-publish
```

```yml
include:
    - project: pektin/pektin-dist
      ref: main
      file:

stages:
```

# Build Image and Publish it to Docker

```yml
include:
    - project: pektin/pektin-dist
      ref: main
      file:
          - scripts/docker-build-and-publish.yml
variables:
    IMAGE_NAME: coolImage # -> pektin/coolImage
stages:
    - docker-build-and-publish
```

# Run `yarn publish` and publish to NPM

```yml
include:
    - project: pektin/pektin-dist
      ref: main
      file:
          - scripts/npm-build-and-publish.yml
stages:
    - npm-build-and-publish
```
