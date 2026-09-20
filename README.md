# CareerSimplify Monorepo

A high-performance full-stack monorepo powered by [Turborepo](https://turbo.build/repo) and [pnpm](https://pnpm.io).

## 🚀 Tech Stack

| Workspace | Technology | Description | Default Port / URL |
| :--- | :--- | :--- | :--- |
| **`apps/web`** | **[Next.js 16](https://nextjs.org/)** (React 19, Turbopack) | Frontend Web Application (App Router) | `http://localhost:3000` |
| **`apps/api`** | **[NestJS 12](https://nestjs.com/)** (TypeScript, Vitest, Oxlint) | Backend REST API Service | `http://localhost:4000` |
| **`apps/mobile`** | **[Expo SDK 57](https://expo.dev/)** (React Native 0.86, Expo Router) | Cross-Platform Mobile Application (iOS, Android, Web) | `http://localhost:8081` |
| **`packages/ui`** | React Component Library | Shared UI components across frontend applications | — |
| **`packages/eslint-config`** | ESLint Flat Config | Shared linting rules across apps & packages | — |
| **`packages/typescript-config`** | TypeScript Configurations | Shared `tsconfig.json` bases across workspace | — |

---

## 📁 Repository Structure

```
careersimplify/
├── apps/
│   ├── api/                    # NestJS Backend API (generated via @nestjs/cli)
│   │   ├── src/
│   │   │   ├── app.controller.ts
│   │   │   ├── app.module.ts
│   │   │   ├── app.service.ts
│   │   │   └── main.ts         # Server entrypoint (default port: 4000)
│   │   ├── test/               # Vitest e2e & unit test suite
│   │   └── package.json
│   │
│   ├── web/                    # Next.js Web App (Next.js 16 + React 19)
│   │   ├── app/                # App Router routes and layouts
│   │   └── package.json
│   │
│   └── mobile/                 # Expo Mobile App (SDK 57 + Expo Router)
│       ├── src/app/            # File-based routes for iOS, Android, and Web
│       ├── assets/             # Images and app icons
│       └── package.json
│
├── packages/
│   ├── ui/                     # Shared UI components library (@repo/ui)
│   ├── eslint-config/          # Shared ESLint configuration (@repo/eslint-config)
│   └── typescript-config/      # Shared TypeScript configs (@repo/typescript-config)
│
├── package.json                # Root package.json with Turborepo scripts
├── pnpm-workspace.yaml         # pnpm workspace configuration
└── turbo.json                  # Turborepo pipeline configuration
```

---

## 🛠️ Prerequisites

- **Node.js**: `>= 24.0.0`
- **pnpm**: `>= 10.0.0` (Recommended: `11.x`)

To install pnpm globally (if not already installed):
```sh
corepack enable pnpm
# or
npm install -g pnpm
```

---

## 📦 Installation

Clone the repository and install all dependencies:

```sh
pnpm install
```

---

## ⚡ Development

### Run all applications concurrently
```sh
pnpm dev
```
Turborepo will start:
- **Next.js Web App**: [http://localhost:3000](http://localhost:3000)
- **NestJS Backend API**: [http://localhost:4000](http://localhost:4000)
- **Expo Mobile Dev Server**: [http://localhost:8081](http://localhost:8081)

### Run a specific application
You can filter execution by app name using Turborepo `--filter`:

```sh
# Start only the NestJS backend
pnpm --filter api dev

# Start only the Next.js frontend
pnpm --filter web dev

# Start only the Expo mobile app
pnpm --filter mobile dev

# Start Expo for specific platforms
pnpm --filter mobile android
pnpm --filter mobile ios
pnpm --filter mobile web
```

---

## 🏗️ Production Build

### Build all apps and packages
```sh
pnpm build
```

### Build a specific app
```sh
# Build NestJS API (outputs to apps/api/dist)
pnpm --filter api build

# Build Next.js Web app (outputs to apps/web/.next)
pnpm --filter web build

# Export Expo static assets / bundles (outputs to apps/mobile/dist)
pnpm --filter mobile build
```

---

## 🧪 Testing & Code Quality

### Run Tests
```sh
# Run tests across workspace
pnpm test

# Run NestJS unit tests
pnpm --filter api test

# Run NestJS e2e tests
pnpm --filter api test:e2e
```

### Type Checking
Run TypeScript type-checks across all apps and packages:
```sh
pnpm check-types
```

### Linting & Formatting
```sh
# Lint all workspaces
pnpm lint

# Format code with Prettier
pnpm format
```

---

## ➕ Adding Dependencies & Packages

### Add a dependency to a specific application
```sh
# Add an npm package to apps/web
pnpm --filter web add axios

# Add an npm package to apps/api
pnpm --filter api add @nestjs/config

# Add a dev dependency to apps/mobile
pnpm --filter mobile add -D @types/react-native
```

### Consume a shared workspace package
To consume `@repo/ui` in an app, reference it in that app's `package.json`:
```json
{
  "dependencies": {
    "@repo/ui": "workspace:*"
  }
}
```

---

## 🔧 Scaffold Reference

The monorepo was scaffolded using the official CLI commands:

- **Turborepo**: `pnpm dlx create-turbo@latest . --package-manager pnpm`
- **NestJS API**: `pnpm dlx @nestjs/cli new api --directory apps/api -p pnpm -g --skip-install --no-observe`
- **Expo App**: `pnpm dlx create-expo-app@latest apps/mobile -y --no-install`
