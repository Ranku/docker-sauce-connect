# Docker Sauce Labs Connect

This docker image runs [Sauce Labs Connect](https://wiki.saucelabs.com/display/DOCS/Sauce+Connect+Proxy) 4.4.10 on Java 8.


## Versions

* 4.4.10, latest

## Docker Hub

[ranku/sauce-connect](https://hub.docker.com/r/ranku/docker-sauce-connect/)

## Usage

It sets the `sc` CLI as the entrypoint so it can be used as a replacement via
an shell alias:

```sh
$ alias sc="docker run --rm -it -p 8000:8000 ranku/sauce-connect"
$ sc -P 8000 -u $SAUCE_USERNAME -k $SAUCE_ACCESS_KEY
```

Or just

```sh
$ docker run --rm -it \
             -p 0.0.0.0:8000:8000 \
             ranku/sauce-connect -P 8000 \
                                 -u $SAUCE_USERNAME \
                                 -k $SAUCE_ACCESS_KEY \
                                 --tunnel-identifier foo
```
