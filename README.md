= Docker

== Usage

All images are distributed on https://hub.docker.com/r/joedayz/[Docker Hub^], by user `joedayz`.

The Docker tags of all images are unique and reliable, i.e. they won't change _ever_. You can rely upon builds being based on a particular image and tag, e.g. `joedayz/open-liberty:javaee7-jdk8-b1`, to always produce the same outcome.

== Concept

Besides the idea to have a repository where to share Docker images used in my presentations, workshops, or demos, all Docker images share similar concepts.

- graceful shutdown and proper handling of Unix signals (`SIGTERM`)
- build configuration via environment variables, e.g. `$DEPLOYMENT_DIR` for application servers

This repository is by no means be an exhaustive repository, not even for modern Java EE application servers.
In many occasions I use the (de-facto) official images, such as `jboss/wildfly`.

== Contribution

Feedback, issues, and PRs welcome!

