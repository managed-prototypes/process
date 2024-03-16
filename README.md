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

- DO PAT for terraform:
  - Create on DO: API -> Tokens -> Generate New Token
    - Token name: `terraform_github_actions`
    - Expiration: `No expire` (to prevent it from expiring over time!)
    - Write: `Yes` (terraform must be able apply changes)
    - Click `Generate Token`
  - Save to password manager
  - Save to GitHub org secrets: Org -> Settings -> Secrets and variables -> Actions
    - `DO_PAT`
- DO S3 (spaces):
  - Create,
  - Save keys to password manager
  - Save keys to GitHub org secrets: `DO_S3_ACCESS_KEY`, `DO_S3_SECRET_KEY`
- DO SSH key:
  - Create (locally), save as `~/.ssh/managed_prototypes`
  - Save public and private keys to password manager
  - Save public key to DO team: Settings -> SSH Keys
  - Save private key to GitHub org secrets: `DO_SSH_PVT_KEY`
- DO PAT for cert manager:
  - Create on DO: API -> Tokens -> Generate New Token
    - Token name: `cert-manager`
    - Expiration: `No expire` (to prevent it from expiring over time!)
    - Write: `Yes` (otherwise, it will hang due to Rate limit exceeded – DO will reject the token)
    - Click `Generate Token`
  - Save to password manager
  - Save to GitHub org secrets: `DO_PAT_CERT_MANAGER`
