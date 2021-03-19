# Tex Live image
# https://hub.docker.com/r/texlive/texlive
FROM texlive/texlive:latest

# Creates user 'tex'
ARG USER_UID=1000
ARG USER_GID=${USER_UID}
RUN useradd -m -s /bin/bash -u ${USER_UID} tex \
  && groupmod --gid ${USER_GID} tex

# Installs sudo and pdftk
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends sudo pdftk

# Allows user tex to sudo without password
RUN echo "tex ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/tex \
  && chmod 0440 /etc/sudoers.d/tex
