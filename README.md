# Oh My Zsh docker images

[![Publish workflow](https://github.com/ohmyzsh/docker/actions/workflows/main.yml/badge.svg)](https://github.com/ohmyzsh/docker/actions/workflows/main.yml)

This repository holds the Dockerfile files for the various docker images hosted in the
[ohmyzsh organization at Docker Hub](https://hub.docker.com/u/ohmyzsh).

The code structure is as follows: each top-level folder with a `Dockerfile` file is named after
the image that will be created (e.g. `zsh` folder for [ohmyzsh/zsh](https://hub.docker.com/r/ohmyzsh/zsh)
image).

Inside this folder there needs to be:

- `Dockerfile` for building the Docker image. See [`ohmyzsh/ohmyzsh`](ohmyzsh/Dockerfile) for
  an example of how to set it up, including metadata `LABEL`s.

- `README.md` which provides information regarding the Docker image. If the image has a README.md
  file, this will be used to automatically update the README in Docker Hub.

There also needs to be a separate build job for each image in the [`.github/workflows/main.yml`](https://github.com/ohmyzsh/docker/actions/workflows/main.yml) file.
