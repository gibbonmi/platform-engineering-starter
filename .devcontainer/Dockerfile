FROM mcr.microsoft.com/vscode/devcontainers/base:bookworm as kind

ARG USERNAME=vscode

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install zsh ca-certificates gnupg -y && \
    apt-get autoremove -y && \
    apt-get clean -y

RUN chown -R ${USERNAME}:${USERNAME} /home/${USERNAME}

WORKDIR /home/${USERNAME}
USER ${USERNAME}

CMD ["sleep", "infinity"]