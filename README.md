# A Docker image for `yamllint`

This repository provides an automated build for a lean [yamllint](https://github.com/adrienverge/yamllint) Docker image.

## Informations

* Based on Python (python:3.7-alpine3.9) official Image [python:3.7-alpine3.9](https://hub.docker.com/_/python/)
* Install [Docker](https://www.docker.com/)

## Installation

Pull the image from the Docker repository.

    docker pull mahaga50/yamllint

## Usage

To lint the file `test.yaml` and All files in folder `dir1` in your current directory:

```
docker run --rm -ti -v $(pwd):/workdir mahaga50/yamllint test.yaml dir1/*.yaml
```

## Build

Optionally install python dependencies at build time :

    docker build --rm -t mahaga50/yamllint .
    docker build --rm --build-arg PYTHON_DEPS="flask_oauthlib>=0.9" -t mahaga50/yamllint .


