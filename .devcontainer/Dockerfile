# Tex Live image
# https://hub.docker.com/r/texlive/texlive
FROM texlive/texlive:latest

ARG USER_UID=1000
ARG USER_GID=${USER_UID}
RUN useradd -m -s /bin/bash -u ${USER_UID} -G sudo tex && groupmod --gid ${USER_GID} tex
