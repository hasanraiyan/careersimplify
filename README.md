# Turborepo Monorepo (NestJS + Next.js + Expo)

A full-stack monorepo managed with [Turborepo](https://turbo.build/repo) and [pnpm](https://pnpm.io).

## Applications & Packages

### `apps/`
- **[`api`](apps/api)**: Backend REST API built with [NestJS](https://nestjs.com/) (created via Nest CLI).
- **[`web`](apps/web)**: Frontend web application built with [Next.js](https://nextjs.org/) (App Router, React 19).
- **[`mobile`](apps/mobile)**: Mobile cross-platform application built with [Expo](https://expo.dev/) (Expo Router SDK 57, React Native).

### `packages/`
- **[`@repo/ui`](packages/ui)**: Shared React UI component library.
- **[`@repo/eslint-config`](packages/eslint-config)**: Shared ESLint configurations.
- **[`@repo/typescript-config`](packages/typescript-config)**: Shared TypeScript `tsconfig.json` configurations.

---

## Getting Started

### Prerequisites
- Node.js `>= 24`
- [pnpm](https://pnpm.io/) (`corepack enable pnpm` or `npm install -g pnpm`)

### Install Dependencies
```sh
pnpm install
```

### Development
Start all applications concurrently with Turborepo:
```sh
pnpm dev
```
Or start a specific app using Turborepo filters:
```sh
# NestJS backend only (port 3000 by default or custom)
pnpm --filter api dev

# Next.js web only (port 3000)
pnpm --filter web dev

# Expo mobile only
pnpm --filter mobile dev
```

### Building
Build all applications and packages:
```sh
pnpm build
```
Or build an individual app:
```sh
pnpm --filter api build
pnpm --filter web build
pnpm --filter mobile build
```

### Type Checking & Linting
```sh
# Typecheck all apps and packages
pnpm check-types

# Lint all apps and packages
pnpm lint
```

### Testing
```sh
# Run tests across workspace
pnpm test

# Run NestJS e2e tests
pnpm --filter api test:e2e
```
