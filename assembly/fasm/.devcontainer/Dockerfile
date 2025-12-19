FROM mcr.microsoft.com/devcontainers/base:debian

# Install build essentials and tools needed for FASM/assembly development
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    build-essential \
    gdb \
    make \
    binutils \
    gcc \
    g++ \
    wget \
    && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Install FASM (Flat Assembler)
# Download latest FASM for Linux x64
RUN wget -q https://flatassembler.net/fasm-1.73.31.tgz -O /tmp/fasm.tgz \
    && mkdir -p /tmp/fasm \
    && tar -xzf /tmp/fasm.tgz -C /tmp/fasm --strip-components=1 \
    && cp /tmp/fasm/fasm /usr/local/bin/fasm \
    && chmod +x /usr/local/bin/fasm \
    && rm -rf /tmp/fasm /tmp/fasm.tgz

ENV PATH=$PATH:/usr/local/bin

