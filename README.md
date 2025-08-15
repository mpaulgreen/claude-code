# Claude Code Quick Reference

A comprehensive guide to Claude Code commands, shortcuts, and configuration files.

## Commands

| Command | Description |
|---------|-------------|
| `/init` | Scan codebase and create CLAUDE.md file in project directory |
| `:#` | Add a memory note (useful to prevent Claude from repeating errors) |
| `\` | Insert new line |
| `/clear` | Clear conversation history and free up context |
| `/compact` | Clear conversation history but keep a summary in context |
| `/resume` | Resume a conversation |
| `/review` | Review a pull request |
| `/memory` | Edit Claude memory files |
| `/export` | Export the current conversation to a file or clipboard |
| `/hooks` | Manage hook configurations for tool events |
| `/ide` | Connect to an IDE |
| `/mcp` | Manage MCP connections and view available servers/tools |
| `ESC` | Interrupt Claude to redirect or correct |
| `ESC ESC` | Rewind conversation to earlier point |
| `@` | Mention files to include their content in requests |

## Bash Commands

Execute bash commands by prefixing with `!` (example: `!pwd`). Type `exit` to quit Claude Code.

## Keyboard Shortcuts

| Shortcut | Description |
|----------|-------------|
| `Shift + Tab` | Toggle between planning and auto-accept mode |
| `Cmd + Shift + Ctrl + 4` (Mac)<br>`Win + Shift + S` (Windows) | Take screenshot |
| `Ctrl + V` | Paste screenshot (may not work on Windows) |

## CLAUDE.md Configuration Files

Claude Code supports multiple configuration files for different scopes:

### Project-Level Files

#### `CLAUDE.md`
- **Purpose**: Project-wide instructions for all team members
- **Created by**: `/init` command
- **Version control**: Should be committed and shared
- **Location**: Project root directory

#### `CLAUDE.local.md`
- **Purpose**: Personal project customizations
- **Version control**: Not shared with team (add to .gitignore)
- **Location**: Project root directory

### Global Configuration

#### `~/.claude/CLAUDE.md`
- **Purpose**: Instructions applied to all projects on your machine
- **Location**: `.claude` folder in home directory
- **Scope**: System-wide settings and preferences

### Directory-Specific Instructions

You can place CLAUDE.md files in subdirectories for component or module-specific instructions.

## MCP (Model Context Protocol) Integration

Add external tools to Claude Code using MCP servers:

```bash
# Add a new MCP server (example: Playwright)
claude mcp add playwright npx @playwright/mcp@latest

# Manage MCP servers and view available tools
/mcp
```

## Thinking
Extended thinking is most valuable for complex tasks such as:

- Planning complex architectural changes
- Debugging intricate issues
- Creating implementation plans for new features
- Understanding complex codebases
- Evaluating tradeoffs between different approaches

The way you prompt for thinking results in varying levels of thinking depth:

- "think" triggers basic extended thinking
- intensifying phrases such as "think more", "think a lot", "think harder", or "think longer" triggers deeper thinking

## Git Worktrees

Git worktrees allow you to work on multiple branches simultaneously:

1. **Create a worktrees folder**: `mkdir .trees`
2. **Add a worktree**: `git worktree add ./trees/ui_feature`
3. **View branches**: `git branch -a`
4. **Work in parallel**: Open terminals for each feature branch
5. **Commit changes**: Add and commit with descriptive messages
6. **Merge branches**: Use `git merge` to merge worktrees and resolve conflicts
7. **Cleanup**: Remove `.trees` folder when done and push to GitHub

## GitHub Integration

| Command | Description |
|---------|-------------|
| `/install-github-app` | Install GitHub app for enhanced integration |
| `/hooks` | Manage hook configurations for GitHub events |

## Resources

- [Sample CLAUDE.md file](https://github.com/https-deeplearning-ai/ragchatbot-codebase/blob/main/CLAUDE.md)
- [Common workflows](https://docs.anthropic.com/en/docs/claude-code/common-workflows)
- [MCP Documentation](https://docs.anthropic.com/en/docs/claude-code/mcp)
- [Extended Thinking Tips](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/extended-thinking-tips)