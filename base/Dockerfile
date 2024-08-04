FROM docker.io/library/debian:bookworm-slim
RUN apt-get update -y -q && \
    apt-get install -y -q \
        clamav \
        clamav-daemon \
        clamav-freshclam && \
    apt-get clean all && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /var/lib/clamav/
