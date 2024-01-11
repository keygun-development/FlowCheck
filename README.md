# FlowCheck GitHub Action

![FlowCheck Icon](Logo.png)

This GitHub Action checks and verifies your project by installing dependencies, running tests, and executing a linter. It is designed to be used in your Continuous Integration (CI) workflow, particularly for PHP and Node.js projects.

## Inputs

- **enableTests** (optional): Enable or disable running tests. Default is `true`.
- **enableLinter** (optional): Enable or disable running the linter. Default is `true`.
- **testCommand** (optional): Command to run tests. Default is `composer run test`.
- **lintCommand** (optional): Command to run the linter. Default is `npm run lint`.

## Example Usage

Create a workflow file (e.g., `.github/workflows/ci.yml`) in your project repository:

```yaml
name: Run Tests and Linter

on:
  pull_request:
    types:
      - opened
      - synchronize

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Flowcheck
        uses: keygun-development/FlowCheck@v3.0.1
        with:
          enableTests: true
          enableLinter: true
          testCommand: 'composer run custom-test-command'
          lintCommand: 'npm run custom-lint-command'
```