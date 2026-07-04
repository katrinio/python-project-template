# Contributing

This is a template repository, but the same workflow applies to any project started from it.

## Setup

```bash
poetry install
poetry run pre-commit install
```

## Before a PR

```bash
poetry run ruff check .
poetry run mypy src
poetry run pytest tests --cov=src
```

All three run in CI on every PR — a red CI won't get merged.

## Style

- business logic lives in `src/`, not scattered across scripts;
- new code needs type hints — `mypy` runs in strict mode (`disallow_untyped_defs`);
- tests are required for new modules and non-trivial logic.

## PR

- keep it small and focused on one thing.
