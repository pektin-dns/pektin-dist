# Mirror to GitHub and GitLab

```yml
include:
    - remote: https://git.y.gy/pektin/pektin-dist/-/raw/main/scripts/mirror.yml
stages:
    - mirror
```

# Build Image and Publish it to Docker

```yml
include:
    - remote: https://git.y.gy/pektin/pektin-dist/-/raw/main/scripts/docker-build-and-publish.yml
variables:
    IMAGE_NAME: coolImage # -> pektin/coolImage
stages:
    - docker-build-and-publish
```

# Run `yarn publish` and publish to NPM

```yml
include:
    - remote: https://git.y.gy/pektin/pektin-dist/-/raw/main/scripts/npm-build-and-publish.yml
stages:
    - npm-build-and-publish
```
