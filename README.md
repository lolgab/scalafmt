# Scalafmt Action

A GitHub Action to run Scalafmt on your Pull Requests and push the results back to your branch.

### Example

```yaml
name: scalafmt

on:
  - pull_request

jobs:
  scalafmt:
    runs-on: ubuntu-22.04
    steps:
      - uses: lolgab/scalafmt@0.0.1
        with:
          repo-token: ${{ secrets.GITHUB_TOKEN }}
```
