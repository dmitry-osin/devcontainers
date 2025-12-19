FROM mcr.microsoft.com/devcontainers/base:debian

# Install dependencies for Erlang/Elixir
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    build-essential \
    curl \
    git \
    inotify-tools \
    && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Install Erlang/OTP
# Retry curl download in case of network issues (504, timeouts, etc.)
RUN for i in 1 2 3 4 5; do \
        curl -fsSL https://packages.erlang-solutions.com/erlang-solutions_2.0_all.deb -o /tmp/erlang-solutions.deb && break || sleep 5; \
    done \
    && dpkg -i /tmp/erlang-solutions.deb \
    && apt-get update \
    && apt-get -y install --no-install-recommends esl-erlang \
    && rm -rf /tmp/erlang-solutions.deb \
    && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Install Elixir
RUN apt-get update \
    && apt-get -y install --no-install-recommends elixir \
    && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Install Hex and Rebar
RUN mix local.hex --force \
    && mix local.rebar --force

ENV PATH=$PATH:/usr/local/bin

