# Jenkins with Docker support

This is a Docker Compose configuration which will download and install Jenkins with Docker support.

## Prerequisites

- [Docker](http://docs.docker.com/installation/#installation)
- [Docker Compose](http://docs.docker.com/compose/)

## Usage

`docker-compose up -d` to start Jenkins.

Use `localhost:8084` to view the Jenkins application. You should see "dind" slave under the "Build Executor Status" section.

You can add `docker version` to a build to verify that Docker is working within Jenkins.

Make sure you check "Restrict where this project can be run" and set it to "dind" in the build so that docker will run on the slave where docker is available.
