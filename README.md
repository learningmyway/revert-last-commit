# revert-last-commit 
The github action will be used to revert last commit . It is the public repo. Please find the release status from below statis badge


[![Release](https://github.com/learningmyway/revert-last-commit/actions/workflows/release-version.yml/badge.svg?branch=main)](https://github.com/learningmyway/revert-last-commit/actions/workflows/release-version.yml)

# Usage

```
on:
  push:
    branches: [ master ]

jobs:
  release:
    runs-on: ubuntu-latest

    steps:
      - name: checkout
        uses: actions/checkout@v2

      - name: delete last commit
        uses: learningmyway/revert-last-commit@v1
        env:
          NPM_TOKEN: ${{ secrets.NPM_TOKEN }}
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

```
