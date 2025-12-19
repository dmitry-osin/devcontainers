FROM mcr.microsoft.com/devcontainers/base:debian

# Install necessary packages
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    curl \
    gzip \
    && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Install Coursier (package manager for Scala)
RUN curl -fL https://github.com/coursier/coursier/releases/latest/download/cs-x86_64-pc-linux.gz | gzip -d > /tmp/cs \
    && chmod +x /tmp/cs \
    && mv /tmp/cs /usr/local/bin/cs

# Install Scala and sbt through Coursier for all users
RUN cs install scala:3.3.1 scalac:3.3.1 sbt:1.9.7 \
    && ln -sf /root/.local/share/coursier/bin/scala /usr/local/bin/scala \
    && ln -sf /root/.local/share/coursier/bin/scalac /usr/local/bin/scalac \
    && ln -sf /root/.local/share/coursier/bin/sbt /usr/local/bin/sbt

ENV PATH=$PATH:/root/.local/share/coursier/bin:/usr/local/bin
ENV SCALA_HOME=/root/.local/share/coursier/bin

