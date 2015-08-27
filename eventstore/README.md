# Supported tags and respective `Dockerfile` links

-   [`3.1.0`, `3.1`, `latest` (*3.1/Dockerfile*)](https://github.com/ruudud/dockerfiles/blob/51c4a163f4b7b9b2a6e2e29316807064a21d5d3b/eventstore/3.1/Dockerfile)

![logo](https://raw.githubusercontent.com/EventStore/Brand/master/Logo.png)

# What is Event Store?

Event Store is an open-source, functional database with Complex Event
Processing in JavaScript. Event Store stores your data as a series of
immutable events over time, making it easy to build event-sourced applications.

# How to use this image

## Start an `eventstore` server instance
Starting an Event Store instance is simple:

    $ docker run --name some-eventstore -d ruudud/eventstore:tag

...where `some-eventstore` is the name you want to assign to your container,
and `tag` is the tag specifying the EventStore version you want. Omit `:tag`
for using latest.


## Environment Variables
When you start the eventstore image, you can adjust the configuration of the
EventStore instance by passing one or more environment variables on the docker
run command line. See the [eventstore docs]
(http://docs.geteventstore.com/server/3.1.0/command-line-arguments/) for the
various options.

Example:

    $ docker run -e EVENTSTORE_WORKER_THREADS=12 -d ruudud/eventstore


## Exposed Volumes
The folders `/data/db` and `/data/logs` are used for persisting data, and are
exposed as Docker Volumes.

