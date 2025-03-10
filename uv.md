# Ultimate UV Cheat Sheet

## Getting Started

- **Auto Installation**: UV automatically downloads Python if it's not available
- **Priority System**: UV prioritizes its own Python installations over system installs, even when its version is older

## Important Paths

- Python Installations: `~/.local/share/uv/python`
- Temporary Tools: `~/.cache/uv`
- Permanent Tools: `~/.local/share/uv/tools`

## Running Python Scripts

- `uv run hello.py` - Execute scripts with UV's default Python

## Temporary Tool Usage

- `uvx ruff` - Run tools on-demand without permanent installation

## Permanent Tool Installation

- `uv tool install ruff` - Install tool permanently
- `ruff` - Run installed tools directly (they're added to your PATH)
