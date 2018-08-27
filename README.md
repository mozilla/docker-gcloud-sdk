# docker-gcloud-sbt
Dockerfile for [Google Cloud SDK](https://cloud.google.com/sdk/) with the beta emulators installed

This is built on top of the [google/cloud-sdk](https://hub.docker.com/r/google/cloud-sdk/) alpine image

## Usage

Install [Docker](https://www.docker.com/) and pull the image ([mozilla/gcloud-sdk-emulators](https://hub.docker.com/r/mozilla/gcloud-sdk-emulators/) on DockerHub):

    docker pull mozilla/gcloud-sdk-emulators

You can then use `gcloud` inside docker to run emulators like:

    docker run -itp 8085:8085 --rm mozilla/gcloud-sdk-emulators gcloud beta emulators pubsub start

## Pushing a new tag to DockerHub

DockerHub automated builds automatically build the `alpine` and `latest` tags on changes to master
