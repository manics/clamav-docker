######################################################################
# Pull the latest freshclam image, update data
ARG FRESHCLAM_IMAGE=ghcr.io/manics/clamav:latest
FROM $FRESHCLAM_IMAGE as update

RUN freshclam --help

######################################################################
# Squash data
ARG BASE_IMAGE=ghcr.io/manics/clamav-base:latest
FROM $BASE_IMAGE as base

USER clamav
COPY --from=update /var/lib/clamav /var/lib/clamav
