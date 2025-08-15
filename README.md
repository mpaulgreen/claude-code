# Claude Code Quick Reference

## Commands

| Command | Description |
|---------|-------------|
| `/init` | Claude Code scans your codebase and creates CLAUDE.md file inside your project directory |
| `:#` | Quickly add a memory. Useful when you see Claude Code repeats an error |
| `\` | New line |
| `/clear` | Clears current conversation history |
| `/compact` | Summarizes current conversation history |
| `ESC` | Interrupt Claude to redirect or correct it |
| `ESC ESC` | Rewind the conversation to an earlier point in time |
| `@` | Mention files with @ to include its content in your request |
| `/mcp` | Manage MCP connection & check available MCP servers with their provided tools |

## Bash Commands

You can use regular bash commands within Claude Code by starting them with `!` (for example: `!pwd`). Type `exit` to quit Claude Code.

## Keyboard Shortcuts

| Shortcut | Description |
|----------|-------------|
| `Shift + Tab` | Switch between planning and auto-accept mode |
| `Cmd + Shift + Ctrl + 4` (Mac) / `Win + Shift + S` (Windows) | Take a screenshot |
| `Ctrl + V` | Paste a screenshot (might not work on Windows) |

## CLAUDE.md Files

Claude Code uses several types of CLAUDE.md files for different purposes:

### CLAUDE.md
- Generated with `/init` command
- Should be committed to source control
- Shared with other engineers
- Location: project directory

### CLAUDE.local.md
- Not shared with other engineers
- Contains personal instructions and customizations for Claude
- Location: project directory

### ~/.claude/CLAUDE.md
- Used for all projects on your machine
- Contains instructions that you want Claude to follow on all projects
- Location: `.claude` folder stored in your home directory

## Resources

- [Sample CLAUDE.md file](https://github.com/https-deeplearning-ai/ragchatbot-codebase/blob/main/CLAUDE.md)