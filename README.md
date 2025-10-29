# Compelete DevOps Pipeline

## Organization

```bash
├── .github/
├── client/
├── infra/
├── scripts/
└── README.md
```

`.github` - Github Workflows (see [below](#github-workflows))

`client` - Vite + React + TypeScript client application

`infra` - Docker compose

## Building for Production

`cd client && bun run build`

This will:
Run `tsc` and `vite build` to compile and bundle the client-side code

## Deploying

### Locally

Run `./scripts/deploy-local.sh` and visit `http://localhost:3000`

## Github Workflows

There are three GitHub workflows set up for this project:

Lint: Runs ESLint on the codebase to ensure code quality and consistency

Build: Builds the project to ensure that there are no compilation errors

Docker (on merge): Builds the Dockerfile and uploads to ghcr.io
