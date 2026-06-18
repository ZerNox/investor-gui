# investor-gui

Investor GUI application.

## Development

This project uses [uv](https://docs.astral.sh/uv/) for dependency management.

```bash
# Install dependencies (incl. dev tools) into a virtualenv
uv sync

# Install the git pre-commit hooks (run once)
uv run pre-commit install

# Run all hooks against every file
uv run pre-commit run --all-files
```

### Pre-commit hooks

Configured in [`.pre-commit-config.yaml`](.pre-commit-config.yaml):

- **gitleaks** — scans staged changes and blocks any commit that would leak a
  secret (API keys, tokens, private keys, …).
- **detect-private-key** plus general hygiene checks (trailing whitespace,
  end-of-file, YAML/TOML validation, large files, merge conflicts).
- **ruff** — linting and formatting.

The hooks run automatically on every `git commit` once installed.
