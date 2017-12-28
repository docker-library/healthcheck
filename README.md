# `HEALTHCHECK`

This is an example set of prototype images (available under https://hub.docker.com/u/healthcheck) for enabling [`HEALTHCHECK`](https://github.com/docker/docker/issues/21142) behavior in the official images.

These images are not maintained and are only provided as a reference in implementing your own `HEALTHCHECK`.

See [docker-library/cassandra#76 (comment)](https://github.com/docker-library/cassandra/pull/76#issuecomment-246054271) for the rationale for why these don't get added to the official images directly.

See [`github.com/docker-library/oi-janky-groovy/healthcheck-pipeline.groovy`](https://github.com/docker-library/oi-janky-groovy/blob/master/healthcheck-pipeline.groovy) for the script which builds and pushes these to the [`healthcheck` namespace on Docker Hub](https://hub.docker.com/u/healthcheck/).
