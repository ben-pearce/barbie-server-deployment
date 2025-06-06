# 🚛 Backup Server Deployment

This repository holds my docker compose files and configuration files for services I host on my backup server. Remote storage repositories are mounted with rclone and incremental backups performed with borgmatic.

## Containers

| **Name** | **Description** | **Ports** | **Links** |
|---|---|---|---|
| [portainer-agent](./docker-compose.monitoring.yml#L5)  | Portainer edge agent. |  | [GitHub](https://github.com/portainer/agent) |
| [zabbix-agent](./docker-compose.monitoring.yml#L21)  | Zabbix agent for monitoring. |  | [Docker Hub](https://hub.docker.com/r/zabbix/zabbix-agent) |
| [borgmatic](./docker-compose.yml#L7)  | Simple, configuration-driven backup software. |  | [GitHub](https://github.com/borgmatic-collective/borgmatic) |
| [rclone](./docker-compose.yml#L42)  | Command-line program to sync files and directories to and from different cloud storage providers. |  | [Website](https://rclone.org/) |



## Prerequisites

A linux-based operating system with [docker](https://docs.docker.com/engine/install/) installed.

## Configuration
The `.env` file stores environment variables to make starting the containers easy. This should be modified to match your needs before starting the containers for the first time.

| **Variable** | **Description** | **Example** |
|---|---|---|
| `SMTP_HOST` | SMTP mail server host. | `mail.example.com` |
| `SMTP_USER` | SMTP username. | `postmaster@example.com` |
| `TZ` | Timezone for all containers. | `Europe/London` |
| `PUID` | System user ID to run containers as. | `1000` |
| `PGID` | System group ID to run containers as. | `1000` |
| `CONFIG_DIR` | Location of config storage on host. | `config` |
| `DATA_DIR` | Location of data storage on host. | `data` |
| `ADMIN_EMAIL` | Administrative email address. | `somebody@example.com` |
| `ZBX_HOSTNAME` | Zabbix server hostname. | `zabbix-server` |
| `ZBX_SERVER_HOST` | Zabbix monitoring server host. | `zabbix` |
| `ZBX_REFRESHACTIVECHECKS` | Zabbix active check interval. | `60` |


## Contributions

First of all, **thanks for your interest!** But due to this being a personal project of mine tailored to my own needs, I cannot accept pull requests on this repository. Please feel free to fork and tweak this project though.