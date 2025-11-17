# === Base image: Maven + JDK 17 (required for Sonar & builds)
FROM maven:3.9.6-eclipse-temurin-17

USER root

# === Install Docker CLI + git (required for docker build/push & git commits)
RUN apt-get update && \
    apt-get install -y --no-install-recommends docker.io git && \
    rm -rf /var/lib/apt/lists/*

# === Directory Jenkins will work from
WORKDIR /workspace

# === Keep entrypoint simple
ENTRYPOINT ["bash", "-lc"]

