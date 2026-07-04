# python-project-template

A clean starting point for small Python projects — the setup I reach for every time instead of copy-pasting configs from an old repo.

---

## What's inside

- `src/` and `tests/` layout, ready for a package
- Poetry for dependency management
- Ruff for linting and formatting
- Mypy in strict mode
- Pytest with coverage
- Pre-commit hooks running the same checks as CI
- GitHub Actions workflow for code style and tests
- `.editorconfig` for consistent formatting across editors
- Issue and PR templates

---

## Stack

- Python 3.14, Poetry
- Ruff, Mypy, Pytest

---

## Using this template

1. Click **Use this template** on GitHub (or `git clone` and re-init).
2. Rename the package in `pyproject.toml` (`[tool.poetry] name` and `packages`).
3. Replace this README with one for your actual project.
4. Update `LICENSE` copyright year/name if needed.

## Quick start

```bash
poetry install
poetry run pre-commit install
```

### Virtual environment on macOS

Install Python 3.14 (if you don't have it yet):

```bash
brew install python@3.14
```

Point Poetry at it and create the venv:

```bash
poetry env use 3.14
poetry install
```

Activate the venv in your shell:

```bash
eval "$(poetry env activate)"
```

To deactivate:

```bash
deactivate
```

`poetry run <command>` works without activating the venv — use activation only if you want commands like `python` or `pytest` to resolve directly.

## Checks

```bash
poetry run ruff check .
poetry run mypy src
poetry run pytest tests --cov=src
```

All three run in CI on every PR — see [CONTRIBUTING.md](CONTRIBUTING.md).
