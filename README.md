# trafficserver

https://hub.docker.com/r/twigley/trafficserver/

Builds a docker image containing Apache Traffic Server.

Runs regression tests on installation as per documentation as part of the build:
https://docs.trafficserver.apache.org/en/latest/getting-started/index.en.html#installing-from-source-code

### Build:

```shell
docker build -t trafficserver .
```

To run:

```shell
docker run -p 80:8080 trafficserver
```

### Config

You can alter specific config by referencing files e.g.

```shell
docker run -p 80:8080 \
-v somewhere/records.config:/opt/trafficserver/etc/records.config \
twigley/trafficserver
```

or just the whole config dir

```shell
docker run -p 80:8080 \
-v /somewhere/:/opt/trafficserver/etc/ \
twigley/trafficserver
```
