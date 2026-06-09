# Local Development & Testing

## Setup

```bash
# Install dependencies
npm install

# Install Git hooks for pre-commit validation
npm run prepare
```

## Running Tests

```bash
# Run tests locally
npm test
```

This executes `test.js`, which starts the test suite with a 3-second delay. The workflow automatically runs the same test on every push via GitHub Actions with npm dependency caching for speed.

## Pre-commit Hooks

The `.husky/pre-commit` hook validates workflow YAML files before you commit. If you modify any `.github/workflows/*.yml`, the hook ensures required fields (`name:`, `on:`, `jobs:`) are present.

To bypass (not recommended):
```bash
git commit --no-verify
```
