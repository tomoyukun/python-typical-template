# Python Project Template

A simple template for starting Python projects.

Give Claude instructions like the following to make it your own Python project:

> Change the project name to "myapp". Set the package name to "myapp", description to "My awesome application", and update the author name.

Files that will be changed:

- pyproject.toml: name, description, authors, known-first-party
- src/dummy/ → src/myapp/
- README.md: title and description
- tools/main.py, tests/test_math.py: import statements
- .envrc.example: PROJECT_NAME

**Supported:** uv, direnv, pytest, mypy, ruff, VSCode

**TODOs:** CI/CD (GitHub Actions)

**Directory Structure**

```
.
├── src/
│   └── dummy/             # Main package
├── tests/                 # Test code
├── tools/                 # Scripts and utility tools
├── ignored/               # Development files (not tracked by git)
├── pyproject.toml         # Project configuration
├── .gitignore             # Git ignore settings
├── .vscode/               # VSCode settings
└── README.md              # This file
```

---

## Setup

### Environment

We have verified reproducibility under the following environment.

- Python 3.11+
- [uv](https://docs.astral.sh/uv/)
- [direnv](https://direnv.net/)

### Install

This project uses [uv](https://docs.astral.sh/uv/) to manage the environment and dependencies.
You can install this project with the following command:

```bash
# Setup direnv
cp .envrc.example .envrc
direnv allow

# Install dependencies
uv sync  # for users
uv sync --extra dev  # for developers
```

## Development

### Testing and Type Checking

```bash
uv run pytest
uv run mypy src/dummy/
```

## Quick Example

```python
# TODO: Add usage example
```
