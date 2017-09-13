# trafficserver

https://hub.docker.com/r/twigley/trafficserver/

To build:

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
docker run -p 80:8080 -v \
/somewhere/records.config:/opt/trafficserver/etc/records.config \
twigley/trafficserver
```

or just the whole config dir

```shell
docker run -p 80:8080 -v \
/somewhere/:/opt/trafficserver/etc/ \
twigley/trafficserver
```
