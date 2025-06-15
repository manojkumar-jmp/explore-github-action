# explore-github-action

Simple examples of GitHub Workflows, Jobs, Steps, and Actions. Learn how to automate CI/CD and other tasks using GitHub Actions.

## Overview

This repository provides easy-to-understand examples demonstrating how to use GitHub Actions to automate tasks such as building, testing, and deploying your code. It is intended for beginners and anyone interested in getting started with CI/CD and automation using GitHub Actions.

## Features

- Example workflow files for typical CI/CD pipelines
- Demonstrates the structure of workflows, jobs, steps, and actions
- Shows how to use both built-in and custom actions
- Clear, commented YAML files for easy learning

## Getting Started

1. **Fork or clone this repository:**
   ```bash
   git clone https://github.com/manojkumar-jmp/explore-github-action.git
   ```

2. **Browse the `.github/workflows/` directory** to see ready-to-use workflow files.

3. **Adapt the examples** to your own repositories and automation needs.

## Example

Below is a basic example of a workflow that runs on every push and prints "Hello, world!":

```yaml
name: Hello World Workflow

on: [push]

jobs:
  say-hello:
    runs-on: ubuntu-latest
    steps:
      - name: Print greeting
        run: echo "Hello, world!"
```

Find more examples in the [`.github/workflows/`](.github/workflows/) directory.

## Documentation

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Workflow syntax for GitHub Actions](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions)

## Contributing

Contributions are welcome! Please open issues or pull requests for improvements or new examples.

## License

This repository is licensed under the MIT License.
