# Cloud Test Plugin - Claude Code Plugins

Claude Code plugins for cloud testing.

## Installation

Run these slash commands inside an interactive Claude Code session (start with `claude`).

### Step 1: Add the marketplace

```
/plugin marketplace add kolov/cloud-test-plugin
```

### Step 2: Install plugins

Install the plugins you need:

```
/plugin install cx-rust@kolov/cloud-test-plugin
```

When prompted, choose the scope:
- **User**: Install for yourself across all projects
- **Project**: Install for all collaborators on the current repository
- **Local**: Install for yourself in the current repository only

## Available Plugins

| Plugin | Description |
|--------|-------------|
| `cx-rust` | Rust coding standards and best practices |

## Verification

After installation, verify plugins are loaded:

```
/plugin
```

Navigate to the **Installed** tab to see your plugins.

## Project Structure

```
.claude-plugin/
  marketplace.json          # Marketplace definition
plugins/
  rust/                     # Rust coding standards plugin
    .claude-plugin/
      plugin.json
    skills/
      coding-standards/
        SKILL.md
```

To add a new plugin, create a new folder under `plugins/` with the same structure and add it to `marketplace.json`.
