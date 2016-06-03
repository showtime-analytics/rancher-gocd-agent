docker-gocd-agent
==================

A image to run GoCD agent. It's based in "rawmind/rancher-jvm8".

## Build

```
docker build -t showtimeanalytics/rancher-gocd-agent:<version> .
```

## Versions

- `16.5.0` [(Dockerfile)](https://github.com/showtimeanalytics/docker-gocd-agent/blob/master/Dockerfile)

## How it works

* The docker has the entrypoint /usr/bin/start.sh, that runs go-server.
* Config params could be modified overriding these env variables:

```
AGENT_MEM="128m"
AGENT_MAX_MEM="256m"
GO_SERVER=<IP_GOSERVER>
GO_SERVER_PORT="8153"
JVM_DEBUG_PORT="5006"
AGENT_WORK_DIR="$GOCD_HOME/work"

```
