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

### Configuration

#### `commit-message`

The commit message to use for the scalafmt changes

default: `style: Run Scalafmt`

#### `files`

Files to run Scalafmt on. Accepts newline separated list of globs

default:
```
**.scala
**.sbt
**.sc
```

#### `user-name`

Git username used to commit the change

default: `github-actions[bot]`

#### `user-email`

Git email used to commit the change

default: `41898282+github-actions[bot]@users.noreply.github.com`

#### `repo-token`

GitHub token to push changes

default: `${{ github.token }}`

The suggested value is: `${{ secrets.GITHUB_TOKEN }}`
