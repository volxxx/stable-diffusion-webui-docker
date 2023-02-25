FROM bash:alpine3.15

RUN apk add --update-cache \
    parallel\
    aria2\
    rsync \
    openssh-client \
    tzdata \
 && rm -rf /var/cache/apk/*

COPY . /docker
RUN chmod +x /docker/download.sh
ENTRYPOINT ["/docker/download.sh"]
