# Ultimate UV Cheat Sheet

## Getting Started

- **Auto Installation**: UV automatically downloads Python if it's not available
- **Priority System**: UV prioritizes its own Python installations over system installs, even when its version is older

## Important Paths

| Category | Path |
|----------|------|
| Python Installations | `~/.local/share/uv/python` |
| Permanent Tools | `~/.local/share/uv/tools` |
| Temporary Tools | `~/.cache/uv` |

## Basics

| **Running Python Scripts** | **Temporary Tool Usage** | **Permanent Tool Installation** |
|------------------------|------------------------|----------------------------|
| `uv run hello.py` - Execute scripts with UV's default Python | `uvx ruff` - Run tools on-demand without permanent installation | `uv tool install ruff` - Install tool permanently |
| | | `ruff` - Run installed tools directly (they're added to your PATH) |
