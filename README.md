# Claude Explorer (ce)

Interactive CLI navigator for Claude Code context objects.

Browse and inspect everything that shapes Claude's working context:

- **CLAUDE.md** files — project instructions and conventions
- **Memory** — cross-conversation project memory (grouped by type)
- **Settings & Permissions** — allow/deny rules, mode, raw config
- **Hooks** — pre/post tool-use automation
- **Slash Commands** — custom user and project commands
- **MCP Plugins** — Model Context Protocol integrations
- **Plans** — implementation plan files

## Install

```bash
# Download the script
curl -fsSL https://raw.githubusercontent.com/radiolithic/claude-explorer/main/ce -o ~/.local/bin/ce
chmod +x ~/.local/bin/ce

# (Optional) Install the slash command for Claude Code
mkdir -p .claude/commands
curl -fsSL https://raw.githubusercontent.com/radiolithic/claude-explorer/main/ce.md -o .claude/commands/ce.md
```

### Requirements

- Python 3.8+
- No pip dependencies — standard library only
- Claude Code installed (`~/.claude/` directory exists)

## Usage

### From the terminal

```bash
ce
```

### From Claude Code

```
/ce
```

### Main Menu

```
CLAUDE EXPLORER (ce) v0.1.0

  1. CLAUDE.md Files        Project instructions & conventions
  2. Memory                 Project memory (cross-conversation)
  3. Settings & Permissions Allow/deny rules, mode, misc config
  4. Hooks                  Pre/post tool-use hooks
  5. Slash Commands         Custom /commands
  6. MCP Plugins            Model Context Protocol integrations
  7. Plans                  Implementation plans

  0. Context Summary        Full snapshot of what Claude sees
```

Navigation follows a numbered-menu pattern: pick a number to drill in, `b` to go back, `q` to quit. File viewer supports `n`/`p`/`t` pagination.

## How it works

`ce` is a read-only tool. It scans standard Claude Code paths (`~/.claude/`) and the current project directory for configuration and context files. It does not modify, create, or delete anything.

It auto-detects the project root (nearest `.git` or `CLAUDE.md`) and resolves the corresponding memory directory, including handling slug variations across renames.

## Disclaimer

This software is provided "as is", without warranty of any kind, express or implied. Not affiliated with, endorsed by, or supported by Anthropic, PBC. Use at your own risk. See [LICENSE](LICENSE) for full terms.

## License

MIT
