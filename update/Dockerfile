ARG CLAMAV_IMAGE=ghcr.io/manics/clamav:latest
ARG BASE_IMAGE=ghcr.io/manics/clamav-base:latest

######################################################################
# Pull the latest freshclam image, update data
FROM $CLAMAV_IMAGE AS update

RUN freshclam --help

######################################################################
# Squash data
ARG BASE_IMAGE
FROM $BASE_IMAGE AS base

USER clamav
COPY --from=update /var/lib/clamav /var/lib/clamav
