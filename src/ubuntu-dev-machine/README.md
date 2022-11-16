# Description
a generic development container suitable for use with tools like coder.

## building
1. install the devcontainer cli `npm install -g @devcontainers/cli`
1. build `devcontainer build --workspace-folder .`

## pushing (manually)
1. login to ghcr with a personal access token `echo $PAT | docker login ghcr.io --username mspiegel31 --password-stdin`
1. build and push image with latest tag: `devcontainer build --workspace-folder . --push true --image-name ghcr.io/mspiegel31/ubuntu-dev-machine:latest`