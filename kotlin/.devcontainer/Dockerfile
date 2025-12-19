FROM mcr.microsoft.com/devcontainers/base:debian

# Install necessary packages
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    curl \
    zip \
    unzip \
    && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Install SDKMAN
RUN curl -s "https://get.sdkman.io" | bash

# Install Kotlin and Gradle through SDKMAN
RUN bash -c "source /root/.sdkman/bin/sdkman-init.sh && \
    sdk install kotlin && \
    sdk install gradle && \
    sdk flush archives && \
    sdk flush temp"

# Move SDKMAN to shared directory and set proper permissions
RUN mv /root/.sdkman /usr/local/sdkman && \
    chmod -R 755 /usr/local/sdkman && \
    chown -R root:root /usr/local/sdkman

# Make SDKMAN available for all users
RUN echo 'export SDKMAN_DIR="/usr/local/sdkman"' >> /etc/profile.d/sdkman.sh && \
    echo '[[ -s "/usr/local/sdkman/bin/sdkman-init.sh" ]] && source "/usr/local/sdkman/bin/sdkman-init.sh"' >> /etc/profile.d/sdkman.sh && \
    echo 'export SDKMAN_DIR="/usr/local/sdkman"' >> /etc/zsh/zshrc && \
    echo '[[ -s "/usr/local/sdkman/bin/sdkman-init.sh" ]] && source "/usr/local/sdkman/bin/sdkman-init.sh"' >> /etc/zsh/zshrc

ENV SDKMAN_DIR=/usr/local/sdkman
ENV PATH=$PATH:/usr/local/sdkman/candidates/kotlin/current/bin:/usr/local/sdkman/candidates/gradle/current/bin

