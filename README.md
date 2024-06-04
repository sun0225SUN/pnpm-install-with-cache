# pnpm-install-with-cache

Action for Github Workflows that installs pnpm install with a cache

How to use in workflow.yml:

```yml
name: dev

on:
  workflow_dispatch:

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Setup node
        uses: actions/setup-node@v4
        with:
          node-version: 20

      - name: Pnpm Install
        uses: yuanze-dev/pnpm-install-with-cache@v2
        with:
          pnpm-version: 9

      - name: Build project
        run: pnpm build
```