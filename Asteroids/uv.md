`uv` is a Python [[Package Manager]], basically a modern replacement for `pip` and `pip-tools`. It's extremely fast (written in Rust) and handles:

- **Installing packages** — `uv pip install pandas`
- **Managing virtual environments** — `uv venv`
- **Locking dependencies** — generates a `uv.lock` file so everyone on the project uses the exact same versions
- **Running scripts** — `uv run script.py`
- **Managing Python versions** — can install and switch between Python versions, similar to `pyenv`

The main selling point over `pip` is **speed** — it can be 10-100x faster when installing packages, which matters a lot in CI/CD pipelines or when setting up environments frequently.

It was made by Astral, the same team behind `ruff` (the fast Python linter).