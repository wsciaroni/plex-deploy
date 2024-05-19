## Background

In learning to automate deployment of Docker containers, I will use this repository to automate the deployment of Plex using GitHub Actions.

## Assumptions

- The Plex host is availabe from the GitHub runner via SSH
- Docker is installed on the desired Plex host
- The Plex host has its firewall configured to allow Plex's ports in

## Environment Varialbes

This setup will require the use of the following environment variables.

| Variable Name | Note |
| ------------- | ---- |
| `SSH_HOST` | The IP of the host to ssh into |
| `SSH_PORT` | The port of the host to ssh into |
| `SSH_USER` | The user of the `SSH_HOST` which will be used |
| `SSH_PRIVATE_KEY ` | The ssh key to use to authenticate with |
| `PLEX_LIBRARY_PATH` | Plex volume for `/config` |
| `PLEX_TV_PATH` | Plex volume for `/tv` |
| `PLEX_MOVIES_PATH` | Plex volume for `/movies` |
| `GH_PAT` | Used to deploy to or retrieve from the GitHub container registry |
| `GH_USERNAME` | GitHub user associated with the `GH_PAT` |
| `GH_DOCKER_IMAGE_NAME` | Name of the image |
