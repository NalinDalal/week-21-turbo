# Turborepo starter

Turborepo is a high-performance monorepo build system specifically designed to overcome the limitations of traditional monorepos. It adds features and optimizations that make managing monorepos easier and faster.

This is an official starter Turborepo.

## Key Features of Turborepo

1. Incremental Builds:

- Only re-builds and re-tests what’s necessary, leveraging a sophisticated dependency graph.

2. Remote Caching:

- Speeds up CI/CD pipelines by sharing build artifacts between local and remote environments.

3. Task Pipelines:

- Defines tasks for builds, tests, or scripts with dependencies to execute them in the right order.

4. Parallel Execution:

- Executes tasks across multiple projects simultaneously, maximizing CPU utilization.

5. Built for JavaScript/TypeScript Ecosystems:

- Supports Yarn, npm, pnpm, and is optimized for tools like Webpack, Vite, and others.

6. Efficient Workflows:

- Automatically deduplicates dependencies and optimizes package management.

## Using turborep

to start run the following command:

```sh
npx create-turbo@latest
? Where would you like to create your Turborepo? week-21-turbo
? Which package manager do you want to use? yarn
```

## What's inside?

This Turborepo includes the following packages/apps:

### Apps and Packages

- `docs`: a [Next.js](https://nextjs.org/) app
- `web`: another [Next.js](https://nextjs.org/) app
- `@repo/ui`: a stub React component library shared by both `web` and `docs` applications
- `@repo/eslint-config`: `eslint` configurations (includes `eslint-config-next` and `eslint-config-prettier`)
- `@repo/typescript-config`: `tsconfig.json`s used throughout the monorepo

Each package/app is 100% [TypeScript](https://www.typescriptlang.org/).

notice the file structure -
`apps`: Directory for application-specific code
`apps` folder has docs/app-a and web/app-b
`packages` : Directory for shared libraries or modules

### Utilities

This Turborepo has some additional tools already setup for you:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting

### Build

To build all apps and packages, run the following command:

```
cd my-turborepo
pnpm build
```

### Develop

To develop all apps and packages, run the following command:

```
cd my-turborepo
pnpm dev
```

### Remote Caching

> [!TIP]
> Vercel Remote Cache is free for all plans. Get started today at [vercel.com](https://vercel.com/signup?/signup?utm_source=remote-cache-sdk&utm_campaign=free_remote_cache).

Turborepo can use a technique known as [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching) to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching you will need an account with Vercel. If you don't have an account you can [create one](https://vercel.com/signup?utm_source=turborepo-examples), then enter the following commands:

```
cd my-turborepo
npx turbo login
```

This will authenticate the Turborepo CLI with your [Vercel account](https://vercel.com/docs/concepts/personal-accounts/overview).

Next, you can link your Turborepo to your Remote Cache by running the following command from the root of your Turborepo:

```
npx turbo link
```

## Useful Links

Learn more about the power of Turborepo:

- [Tasks](https://turbo.build/repo/docs/core-concepts/monorepos/running-tasks)
- [Caching](https://turbo.build/repo/docs/core-concepts/caching)
- [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching)
- [Filtering](https://turbo.build/repo/docs/core-concepts/monorepos/filtering)
- [Configuration Options](https://turbo.build/repo/docs/reference/configuration)
- [CLI Usage](https://turbo.build/repo/docs/reference/command-line-reference)
