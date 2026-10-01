# review-proof

Runs on `ubuntu-latest` (or another Ubuntu LTS runner) only.

Licensed under [Apache License 2.0](LICENSE).

## Usage

```yaml
name: review-proof
on:
  pull_request_review:
    types: [submitted]

permissions:
  pull-requests: write

jobs:
  review-proof:
    runs-on: ubuntu-latest
    steps:
      - uses: ftsrg-softeng/review-proof-action@master
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
```
