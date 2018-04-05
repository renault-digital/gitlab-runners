FROM node:9.4.0-alpine


ENV ALPINE_VERSION edge
ENV NODE_VERSION 9.4.0
ENV CHROMIUM_VERSION 61
ENV FREETYPE_VERSION 2.8.1-r2
ENV HARFBUZZ_VERSION 1.6.3-r0
ENV CHROME_BIN /usr/bin/chromium-browser

# Install Node & Chromium
RUN apk add \
    --update --no-cache \
    "chromium>=${CHROMIUM_VERSION}" \
    "chromium-chromedriver>=${CHROMIUM_VERSION}" \
    "freetype>=${FREETYPE_VERSION}" \
    "harfbuzz>=${HARFBUZZ_VERSION}" \
    udev \
    git \ 
    bash \
    curl \
    --update-cache \
    --repository "http://dl-cdn.alpinelinux.org/alpine/${ALPINE_VERSION}/main" \
    --repository "http://dl-cdn.alpinelinux.org/alpine/${ALPINE_VERSION}/community" && \
    rm /var/cache/apk/*
