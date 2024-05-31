# pnpm-install-with-cache

Action for Github Workflows that installs pnpm install with a cache

How to use in workflow.yml:

```yml
name: Build client
on:
  push:
    branches: [ main ]

jobs:
  build:
    name: Run pnpm Build
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Install pnpm
        uses: yuanze-dev/pnpm-install-with-cache

      - name: Build client
        run: pnpm build
```