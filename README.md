# Process

## Revisiting repo

- Whenever we update dependencies, we strive to update all repos

## Repo Checklist

- Docs
  - Goals
  - Deployment
  - Development
    - Development Prerequisites
    - Local Dev Workflow
    - Deployment Prerequisites
    - Deployment from local to DO
  - Dev Decisions
  - Updating Dependencies
- Just
- Dockerfile, docker-compose setup
- GH Actions
  - Publish Docker Images, manually and when pushed to main (e.g. pr merged)
  - Deploy
  - Destroy
  - Telegram Notification for new PRs
  - Check and Build for PRs

## Repo Checklist (WIP)

- Automatically create and destroy services in DO (Terraform?)
- domain and a collection of subdomains, 1 per prototype
- e2e testing (cypress) (in k8s)
- integration tests (with testcontainers)
- unit tests (in k8s)
- ui tests (cypress + percy) (in k8s)
- load testing (k6 + grafana) (in k8s)
- schema
- collection of functional requirements to use in several prototypes: helo world, increment int, multiplayer tic tac toe (pvp) with websockets, multi-user chat
