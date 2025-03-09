# UV Cheat Sheet

> An extremely fast Python package and project manager, written in Rust.

- `uv` by default, will use its own versions before using the system version.

### Use case: Run a random python script

| Command | Description |
|---------|-------------|
| `uv run hello.py` | Runs script with default Python version. Auto download latest if none available. |
| `uv run --python 3.08 hello.py` | Runs script with Python 3.08. Auto download if it cannot find version. |
| `~/.local/share/uv/python` | Python installation path |

### Use case: Temporary Python CLI tool install

| Command | Description |
|---------|-------------|
| `uvx ruff` | Runs tool with default Python version. Auto download latest if none available. |
| `uvx --python 3.08 ruff` | Runs tool with Python 3.08. Auto download if it cannot find version. |
| `~/.local/share/uv/python` | Python installation path |
| `~/.cache/uv` | Temp tool path |

### Use case: Permanent Python CLI tool install

| Command | Description |
|---------|-------------|
| `uv tool install ruff` | Installs tool with default Python version. Auto download latest if none available. |
| `uv tool install --python 3.08 ruff` | Installs tool with Python 3.08. Auto download if it cannot find version. |
| `ruff` | The tool is in the PATH, so call it directly. |
| `~/.local/share/uv/python` | Python installation path |
| `~/.local/share/uv/tools` | Tool installation path |
