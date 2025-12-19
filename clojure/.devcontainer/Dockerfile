FROM mcr.microsoft.com/devcontainers/base:debian

# Install Java (required for Clojure)
# Try openjdk-17-jdk first, fallback to default-jdk if not available
RUN export DEBIAN_FRONTEND=noninteractive \
    && apt-get update \
    && (apt-get -y install --no-install-recommends openjdk-17-jdk || apt-get -y install --no-install-recommends default-jdk) \
    && apt-get -y install --no-install-recommends \
    curl \
    rlwrap \
    ca-certificates \
    && apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*

# Install Clojure CLI tools
RUN curl -O https://download.clojure.org/install/linux-install-1.11.1.1347.sh \
    && chmod +x linux-install-1.11.1.1347.sh \
    && ./linux-install-1.11.1.1347.sh \
    && rm linux-install-1.11.1.1347.sh

ENV CLOJURE_HOME=/usr/local/lib/clojure
ENV PATH=$PATH:$CLOJURE_HOME/bin

