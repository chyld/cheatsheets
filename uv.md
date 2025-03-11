# Ultimate UV Cheat Sheet

## Configuration

`~/.config/uv/uv.toml`

| Setting | Purpose |
|------|---------|
| `python-preference = "only-managed"` | Only use managed Python installations; never use system Python installations |

## Installing Python

| Use case | Command |
|--------------|-------------|
| Installing a specific Python version | `uv python install 3.12` |
| List available Python versions. If you use `only-managed` in your config, you will not see any system installs. | `uv python list` |

## Basics

| **Running Python Scripts** | **Temporary Tool Usage** | **Permanent Tool Installation** |
|------------------------|------------------------|----------------------------|
| `uv run hello.py` - Execute scripts with UV's default Python | `uvx ruff` - Run tools on-demand without permanent installation | `uv tool install ruff` - Install tool permanently |
| | | `ruff` - Run installed tools directly (they're added to your PATH) |

## Important Paths

| Category | Path |
|----------|------|
| Python Installations | `~/.local/share/uv/python` |
| Permanent Tools | `~/.local/share/uv/tools` |
| Temporary Tools | `~/.cache/uv` |

## Notes

- **Auto Installation**: UV automatically downloads Python if it's not available
- **Priority System**: UV prioritizes its own Python installations over system installs, even when its version is older
