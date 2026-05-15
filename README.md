# `op_run` command

`op_run` wrap `op run` at Linux or MacOS and `oprun` at WSL (Windows Subsystem for Linux).

## Dependency

- Linux or MacOS -> `op run` exists
- WSL (WindowsOS) -> `oprun` ([pollenjp/oprun.sh](https://github.com/pollenjp/oprun.sh)) exists

  On WSL, `op_run` calls `oprun` from [pollenjp/oprun.sh](https://github.com/pollenjp/oprun.sh)
  under the hood, so you need to install it as well. The easiest way is via
  [mise](https://mise.jdx.dev/):

  ```bash
  # Latest release
  mise use -g github:pollenjp/oprun.sh

  # Pinned version
  mise use -g github:pollenjp/oprun.sh@v0.2.0
  ```

  Or in `mise.toml`:

  ```toml
  [tools]
  "github:pollenjp/oprun.sh" = "latest"
  ```

## Installation

### Option 1: mise (via the GitHub backend)

If you use [mise](https://mise.jdx.dev/), you can install `op_run` from the
[GitHub backend](https://mise.jdx.dev/dev-tools/backends/github.html):

```bash
# Latest release
mise use -g github:pollenjp/op_run

# Pinned version
mise use -g github:pollenjp/op_run@v0.2.0
```

Or in `mise.toml`:

```toml
[tools]
"github:pollenjp/op_run" = "latest"
```

### Option 2: Install script

```bash
op_run_path=~/.local/bin/op_run
mkdir -p "${op_run_path%/*}"
curl -fsSL https://raw.githubusercontent.com/pollenjp/op_run/main/op_run \
  -o "${op_run_path:?}"
chmod +x "${op_run_path:?}"
```
