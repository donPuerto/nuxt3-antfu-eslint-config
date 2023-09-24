# Nuxt 3 Eslint configuration

Eslint [Antfu](https://github.com/antfu/eslint-config) configuration.

## Setup

Make sure to install the dependencies:

```bash
# npm
npm install -D eslint @antfu/eslint-config

# pnpm
pnpm add -D eslint @antfu/eslint-config

# yarn
yarn add -D eslint @antfu/eslint-config

# bun
bun install eslint @antfu/eslint-config
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm run dev

# yarn
yarn dev

# bun
bun run dev
```

## VS Code setting
```bash
  {
    // Enable the flat config support
    "eslint.experimental.useFlatConfig": true,

    // Disable the default formatter
    "prettier.enable": false,
    "editor.formatOnSave": false,

    // Auto fix
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true,
      "source.organizeImports": false
    },

    // Silent the stylistic rules in you IDE, but still auto fix them
    "eslint.rules.customizations": [
      { "rule": "@stylistic/*", "severity": "off" },
      { "rule": "style*", "severity": "off" },
      { "rule": "*-indent", "severity": "off" },
      { "rule": "*-spacing", "severity": "off" },
      { "rule": "*-spaces", "severity": "off" },
      { "rule": "*-order", "severity": "off" },
      { "rule": "*-dangle", "severity": "off" },
      { "rule": "*-newline", "severity": "off" },
      { "rule": "*quotes", "severity": "off" },
      { "rule": "*semi", "severity": "off" }
    ],

    // The following is optional.
    // It's better to put under project setting `.vscode/settings.json`
    // to avoid conflicts with working with different eslint configs
    // that does not support all formats.
    "eslint.validate": [
      "javascript",
      "javascriptreact",
      "typescript",
      "typescriptreact",
      "vue",
      "html",
      "markdown",
      "json",
      "jsonc",
      "yaml"
    ]
  }
```
