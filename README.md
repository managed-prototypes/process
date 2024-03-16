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
- domain and a collection of subdomains, 1 per prototype
- e2e testing (cypress) (in k8s)
- integration tests (with testcontainers)
- unit tests (in k8s)
- ui tests (cypress + percy) (in k8s)
- load testing (k6 + grafana) (in k8s)
- schema
- collection of functional requirements to use in several prototypes:
  - helo world,
  - increment int (including POST requests with CORS)
  - multiplayer tic tac toe (pvp) with websockets
  - multi-user chat
  - multi-user note-taking app

## Bonus: Initial setup, once per DO team (in commercial practice – 1 DO team per separate project)

- DO PAT for terraform: create, save to password manager, save to GitHub org secrets
- DO S3 (spaces): create, save keys to password manager, save keys to GitHub org secrets
- DO SSH key: create locally, save public and private to password manager, save private to GitHub org secrets, save public to DO team (Settings -> SSH Keys)
- DO PAT for cert manager: create, save to password manager, save to GitHub org secrets
