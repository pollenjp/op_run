# `op_run` command

`op_run` wrap `op run` at Linux or MacOS and `oprun` at WSL (Windows Subsystem for Linux).

## Dependency

- Linux or MacOS -> `op run` exists
- WSL (WindowsOS) -> `oprun` ([pollenjp/oprun.sh](https://github.com/pollenjp/oprun.sh)) exists

## Install script

```bash
op_run_path=~/.local/bin/op_run
mkdir -p "${op_run_path%/*}"
curl -fsSL https://raw.githubusercontent.com/pollenjp/op_run/main/op_run \
  -o "${op_run_path:?}"
chmod +x "${op_run_path:?}"
```
