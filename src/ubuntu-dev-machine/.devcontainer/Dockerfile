FROM mcr.microsoft.com/devcontainers/base:ubuntu-20.04

ARG OLD_USERNAME=vscode
ARG USERNAME=mike

# rename base image default
RUN usermod -l $USERNAME --move-home --home /home/$USERNAME $OLD_USERNAME \
    && groupmod --new-name $USERNAME $OLD_USERNAME \
    && echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

USER $USERNAME
