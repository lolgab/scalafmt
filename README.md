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
      - uses: lolgab/scalafmt@main
        with:
          repo-token: ${{ secrets.GITHUB_TOKEN }}
```
