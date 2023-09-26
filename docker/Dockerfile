# It's ya boy: I N F R A
# Dockerfile with SteamRT3 
FROM        registry.gitlab.steamos.cloud/steamrt/sniper/platform 
LABEL       author="Liam C" maintainer="infra@gflclan.com"
LABEL       org.opencontainers.image.source="https://gitlab.gflclan.com/infra/cs2-pterodactyl"

# Prep OS
RUN         mkdir -p /etc/sudoers.d && echo "%sudo ALL=(ALL:ALL) NOPASSWD: ALL" > /etc/sudoers.d/flatdeb && chmod 0440 /etc/sudoers.d/flatdeb
ENV         DEBIAN_FRONTEND=noninteractive
USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

# To-Do: Build Proton
# RUN         apt update && apt install -y git
# RUN         git clone --recurse-submodules https://github.com/ValveSoftware/Proton.git proton && cd proton && make install

# Grab latest SteamRT3 from Valve manually
#RUN         wget https://repo.steampowered.com/steamrt-images-sniper/snapshots/latest-container-runtime-public-beta/com.valvesoftware.SteamRuntime.Sdk-amd64%2Ci386-sniper-sysroot.tar.gz
#ADD         com.valvesoftware.SteamRuntime.Platform-amd64,i386-sniper-sysroot.tar.gz /

# EP
COPY        ./docker/entrypoint.sh /entrypoint.sh
CMD         [ "/bin/bash", "/entrypoint.sh" ]

