Claude Explorer — Interactive navigator for Claude Code context objects.

Run the Claude Explorer script to let the user browse their Claude context interactively:

Execute: ce "$ARGUMENTS"

The explorer provides menu-driven access to:
- CLAUDE.md files (project instructions)
- Memory files (cross-conversation project memory)
- Settings & permissions (allow/deny rules, mode)
- Hooks (pre/post tool-use automation)
- Slash commands (custom /commands)
- MCP plugins (Model Context Protocol integrations)
- Plans (implementation plans)
- Context summary (full snapshot of what Claude sees)

When invoked without arguments, it opens the interactive main menu.
When invoked with a number (e.g., /ce 2), it jumps directly to that section:
  0 = Context Summary, 1 = CLAUDE.md, 2 = Memory, 3 = Settings,
  4 = Hooks, 5 = Commands, 6 = Plugins, 7 = Plans
