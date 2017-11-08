FROM renaultdigital/gitlab-runner-base

ENV ELIXIR_VERSION 1.4.2

RUN set -ux && \
  apk --update add erlang && \
  wget --no-check-certificate https://github.com/elixir-lang/elixir/releases/download/v${ELIXIR_VERSION}/Precompiled.zip && \
  mkdir -p /opt/elixir-${ELIXIR_VERSION}/ && \
  unzip Precompiled.zip -d /opt/elixir-${ELIXIR_VERSION}/ && \
  rm Precompiled.zip && \
  apk --update add erlang-crypto erlang-syntax-tools erlang-parsetools erlang-inets erlang-ssl erlang-public-key erlang-eunit \
  erlang-asn1 erlang-sasl erlang-erl-interface erlang-dev && \
  rm -rf /var/cache/apk/* && \
  export PATH=$PATH:/opt/elixir-${ELIXIR_VERSION}/bin && \
  /opt/elixir-${ELIXIR_VERSION}/bin/mix local.hex --force && \
  /opt/elixir-${ELIXIR_VERSION}/bin/mix local.rebar --force

ENV PATH ${PATH}:/opt/elixir-${ELIXIR_VERSION}/bin
