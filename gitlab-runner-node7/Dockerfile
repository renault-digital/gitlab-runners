FROM renaultdigital/gitlab-runner-base


ENV ALPINE_VERSION edge
ENV NODE_VERSION 7.10.1-r0
ENV CHROMIUM_VERSION 61
ENV FREETYPE_VERSION 2.8.1-r2
ENV HARFBUZZ_VERSION 1.6.3-r0
ENV CHROME_BIN /usr/bin/chromium-browser

# Install Node & Chromium
RUN apk add \
    --update \
    "nodejs-current=${NODE_VERSION}" \
    "nodejs-current-npm=${NODE_VERSION}" \
    "chromium>=${CHROMIUM_VERSION}" \
    "chromium-chromedriver>=${CHROMIUM_VERSION}" \
    udev \
    ttf-freefont \
    --update-cache \
    --repository "http://dl-cdn.alpinelinux.org/alpine/${ALPINE_VERSION}/community" && \
    apk add \
    --update \
    --update-cache \
    "freetype>=${FREETYPE_VERSION}" \
    "harfbuzz>=${HARFBUZZ_VERSION}" \
    --repository "http://dl-cdn.alpinelinux.org/alpine/${ALPINE_VERSION}/main" && \
    rm /var/cache/apk/*
