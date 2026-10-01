# review-proof

Runs on `ubuntu-latest` (or another Ubuntu LTS runner) only.

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
      - uses: <org>/review-proof-action@v1
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
```
