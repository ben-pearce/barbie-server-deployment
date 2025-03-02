# 🚛 Backup Server Deployment

This repository holds my docker compose files and configuration files for services I host on my backup server. Remote storage repositories are mounted with rclone and incremental backups performed with borgmatic.

## Containers

{containers}

## Prerequisites

A linux-based operating system with [docker](https://docs.docker.com/engine/install/) installed.

## Configuration
The `.env` file stores environment variables to make starting the containers easy. This should be modified to match your needs before starting the containers for the first time.

{envs}

## Contributions

First of all, **thanks for your interest!** But due to this being a personal project of mine tailored to my own needs, I cannot accept pull requests on this repository. Please feel free to fork and tweak this project though.