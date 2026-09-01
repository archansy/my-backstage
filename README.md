# my-backstage

Backstage developer portal workspace based on the official Backstage app template.

## Prerequisites

- Node.js `22` or `24` (see `engines.node` in [package.json](package.json))
- Yarn `4.13.0` (managed with Corepack)

## Getting Started

Install dependencies:

```sh
corepack enable
yarn install
```

Run the app locally (frontend + backend):

```sh
yarn start
```

By default, Backstage runs at:

- Frontend: `http://localhost:3000`
- Backend: `http://localhost:7007`

## Common Scripts

From the repository root:

- `yarn start` - Start app and backend in development mode
- `yarn test` - Run tests
- `yarn test:e2e` - Run Playwright end-to-end tests
- `yarn lint:all` - Lint all workspaces
- `yarn build:all` - Build all workspace packages
- `yarn build-image` - Build backend Docker image

## Workspace Layout

- `packages/app` - Backstage frontend app
- `packages/backend` - Backstage backend service
- `plugins` - Internal/custom plugins workspace
- `examples` - Sample catalog entities and scaffolder template

## Configuration

- `app-config.yaml` - Local/default configuration
- `app-config.production.yaml` - Production overrides

Update these files for auth providers, catalog locations, integrations, and database settings.

## Notes

- This repository uses Yarn workspaces with Backstage CLI.
- If command resolution fails, run `corepack enable` once and retry.
