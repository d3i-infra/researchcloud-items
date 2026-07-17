# researchcloud-items

This repository contains [Ansible](https://docs.ansible.com) installation scripts for the D3I project for use in conjunction with [SURF ResearchCloud](https://portal.live.surfresearchcloud.nl). 

## Component configuration

https://servicedesk.surf.nl/wiki/display/WIKI/Create+your+own+catalog+items

## Catalog item configuration

SRC-OS
SRC-CO
SRC-Nginx
SRC-External plugin
Your components

## Local testing

To test the self-hosted setup locally, use the compose file in the [mono](https://github.com/d3i-infra/mono) repo:

```bash
docker compose -f docker-compose.selfhosted.local.yml up --build
```

This builds the image, runs database migrations and seeds, and starts the app on `http://localhost:8000`. All values are inlined so no `.env` file is needed.

To reset the database and start fresh:

```bash
docker compose -f docker-compose.selfhosted.local.yml down -v
docker compose -f docker-compose.selfhosted.local.yml up --build
```
