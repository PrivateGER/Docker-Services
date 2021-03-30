# Docker Compose File

# Usage

## Bitwarden
ADMIN_TOKEN: Populate with `openssl rand -base64 64`
domain_origin: Set to base domain

## Grafana
GF_INSTALL_PLUGINS: Set to plugins you want installed, comma seperated
GF_DASHBOARDS_MIN_REFRESH_INTERVAL: minimum global refresh rate

# Portmap
|Service       | Listening address|
|--------------|------------------|
|Grafana       | 127.0.0.1:3456   |
|Loki          | 127.0.0.1:3100   |
|Bitwarden     | 127.0.0.1:6464   |

# Network
Default network is `docker_services`, with all containers but bitwarden_rs connected to it.
Use a reverse proxy (for example nginx) to make locally listening services public.