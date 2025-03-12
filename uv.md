# Ultimate UV Cheat Sheet

## Configuration

| Setting | Purpose |
|------|---------|
| `~/.config/uv/uv.toml` | User-level UV config file |
| `python-preference = "only-managed"` | Only use managed Python installations; never use system Python installations |

## Basics

| Command | Purpose |
|---------|---------|
| `uv python install 3.12` | Installing a specific Python version |
| `uv python list` | List available Python versions |
| `uv run main.py` | Execute Python script |
| `uvx ruff` | Use tool temporarily without installation |
| `uv tool install ruff && ruff` | Install tool permanently and run directly (it is added to your PATH) |

## Creating Projects

| Command | Action |
|---------|--------|
| `uv init my-app` | Create a new project |
| `cd my-app` | Navigate to project |
| `uv run main.py` | Run the main script |
| `uv add numpy pandas` | Add packages |
| `uv tree` | View dependency tree |

## Important Paths

| Category | Path |
|----------|------|
| Python Installations | `~/.local/share/uv/python` |
| Permanent Tools | `~/.local/share/uv/tools` |
| Temporary Tools | `~/.cache/uv` |
| Project Dependencies | `PROJECT_HOME/.venv` |

## Notes

- **Auto Installation**: UV automatically downloads Python if it's not available
- **Priority System**: UV prioritizes its own Python installations over system installs, even when its version is older
