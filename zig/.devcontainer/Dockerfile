FROM mcr.microsoft.com/devcontainers/base:debian

# Install necessary dependencies
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    wget \
    xz-utils \
    ca-certificates \
    && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Install Zig (latest stable version)
# Using a specific version - update as needed for latest
ARG ZIG_VERSION=0.13.0
RUN wget "https://ziglang.org/download/${ZIG_VERSION}/zig-linux-x86_64-${ZIG_VERSION}.tar.xz" \
    && tar -xf "zig-linux-x86_64-${ZIG_VERSION}.tar.xz" -C /usr/local \
    && rm "zig-linux-x86_64-${ZIG_VERSION}.tar.xz" \
    && mv "/usr/local/zig-linux-x86_64-${ZIG_VERSION}" /usr/local/zig

# Add Zig to PATH
ENV PATH="/usr/local/zig:${PATH}"

