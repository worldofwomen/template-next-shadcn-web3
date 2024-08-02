# wmn

# Initialization

This project has been initialized with `npx create-next-app@latest`.

# Configuration

1. Install [nvm](https://github.com/nvm-sh/nvm) if you don't have it.

2. Ensure you're using the node version used in production. From the root directory of the repo, execute the following command:

```bash
nvm use
```

3. The project is configured to run only with the package manager [yarn](https://yarnpkg.com/getting-started/install).

4. Install dependencies:

```bash
yarn
```

5. This project uses [Tailwind CSS](https://tailwindcss.com/docs/installation) in combination with some plugins [ESLint](https://github.com/francoismassart/eslint-plugin-tailwindcss/issues) and [Prettier](https://github.com/tailwindlabs/prettier-plugin-tailwindcss) for formatting.

   > 👋 VSCode/ESLint does not pick newly installed packages in the node_modules directory. After installing the packages for the first time, restart the VSCode workspace.

6. Run the development server:

```bash
yarn dev
```

7. Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

# CI

1. Commit rules:  
   • This repo uses [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/#why-use-conventional-commits) standard  
   • and [commitlint](https://github.com/conventional-changelog/commitlint#benefits-using-commitlint) executed in a husky hook to check them

```bash
# wrong example
git commit -m "add commitlint"
⏳   input: add commitlint
❌   subject may not be empty [subject-empty]
❌   type may not be empty [type-empty]
❌   found 2 problems, 0 warnings
ℹ️   Get help: https://github.com/conventional-changelog/commitlint/#what-is-commitlint
husky - commit-msg hook exited with code 1 (error)
# good example
git commit -m "ci: add commitlint"
```

# Supabase

Before running theses command, start by link your local client to the project.

```bash
yarn supabase login
yarn supabase link
```

Generate types for the project to produce the types/supabase.ts file.

```bash
yarn typegen
```
