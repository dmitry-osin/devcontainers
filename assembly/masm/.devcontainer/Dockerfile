FROM mcr.microsoft.com/devcontainers/base:debian

# Install build essentials and tools needed for MASM/assembly development
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    build-essential \
    nasm \
    gdb \
    make \
    binutils \
    && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Note: MASM (Microsoft Macro Assembler) is Windows-specific and requires
# Visual Studio Build Tools or Windows SDK. For Linux, NASM (Netwide Assembler)
# is installed as an alternative. If you need MASM specifically, consider using
# a Windows-based devcontainer or Wine.

ENV PATH=$PATH:/usr/local/bin

