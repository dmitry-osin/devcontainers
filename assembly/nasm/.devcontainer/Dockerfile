FROM mcr.microsoft.com/devcontainers/base:debian

# Install NASM and development tools
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    nasm \
    build-essential \
    gdb \
    make \
    binutils \
    gcc \
    g++ \
    && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

ENV PATH=$PATH:/usr/local/bin

