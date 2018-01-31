# Renault Digital GitLab runners

Basic alpine images builded with build requirements for several languages, tools and platforms.

This repository is mirrored on GitHub by GitLab: https://github.com/renault-digital/gitlab-runners

Dockers are publicly hosted on https://hub.docker.com/u/renaultdigital/ 

The renaultdigital organization on Dockerhub is integrated with the renault-digital GitHub organization. 
Automatic builds are triggered for the gitlab-runners at each commit.
An an automatic build is set up by runner.

## Docker tags:
- A commit in the master branch produces a docker with "latest" tag.
- A tagged commit from any branch produces a docker with the same tag.



## To add a new runner

- Connect to the Docker Hub with the admin account (cf pass)
- Create a new automated build
- Set the Dockerfile path in Build settings (master branch and tag)
- Push your code or trigger the build webhook