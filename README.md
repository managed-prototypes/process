# Process

## Repo Checklist

- Docs
  - Design
  - Prerequisites
  - Deployment via GH Actions
  - Deployment via CLI
- Justfile

### Repo Checklist (when has some code)

- Dockerfile, docker-compose setup
- Docs
  - Local Dev Workflow
  - Dev Decisions
  - Updating Dependencies
- GH Actions
  - Publish Docker Images, manually and when pushed to main (e.g. pr merged)
  - Deploy
  - Destroy

## When Creating a New Repo

- Set application name in Readme
- Set s3 path for TF state
- Set dns record name in `variables.tf`
- Set example urls
- Check through all the docs

## When Revisiting Repos

- Whenever we update dependencies, we strive to update all repos

## Repo Checklist (WIP)

- Telegram Notification for new PRs (but will there ever be outside collaborators?)
- Check and Build for PRs (but will there ever be outside collaborators?)
- Automatically create and destroy services in DO (Terraform?)
- domain and a collection of subdomains, 1 per prototype
- e2e testing (cypress) (in k8s)
- integration tests (with testcontainers)
- unit tests (in k8s)
- ui tests (cypress + percy) (in k8s)
- load testing (k6 + grafana) (in k8s)
- schema
- collection of functional requirements to use in several prototypes: helo world, increment int, multiplayer tic tac toe (pvp) with websockets, multi-user chat
