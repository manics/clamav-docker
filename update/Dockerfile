######################################################################
# Pull the latest freshclam image, update data
ARG CLAMAV_IMAGE=ghcr.io/manics/clamav:latest
FROM $CLAMAV_IMAGE AS update

RUN freshclam --help

######################################################################
# Squash data
ARG BASE_IMAGE=ghcr.io/manics/clamav-base:latest
FROM $BASE_IMAGE AS base

USER clamav
COPY --from=update /var/lib/clamav /var/lib/clamav
