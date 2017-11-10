FROM renaultdigital/gitlab-runner-base


ENV ALPINE_VERSION edge
ENV NODE_VERSION 8.9.1-r0
ENV CHROMIUM_VERSION 61
ENV FREETYPE_VERSION 2.8.1-r2

# Install Node & Chromium
RUN apk add \
    --update \
    "nodejs=${NODE_VERSION}" \
    "nodejs-npm=${NODE_VERSION}" \
    --update-cache \
    --repository "http://dl-cdn.alpinelinux.org/alpine/${ALPINE_VERSION}/main" \
    --repository "http://dl-cdn.alpinelinux.org/alpine/${ALPINE_VERSION}/community" && \
    rm /var/cache/apk/* && \
    npm install -g gitbook-cli


