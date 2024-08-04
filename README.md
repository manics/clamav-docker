# ClamAV Docker

[![Build](https://github.com/manics/clamav-docker/actions/workflows/build.yml/badge.svg)](https://github.com/manics/clamav-docker/actions/workflows/build.yml)

A [ClamAV](https://www.clamav.net/) container image with up to date signature databases.

```
docker run -it --rm ghcr.io/manics/clamav:latest
```

Note `ghcr.io/manics/clamav:latest` is not built from scratch to avoid overloading the ClamAV database servers.
Instead the previous `latest` image is updated and squashed.
