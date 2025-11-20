# mfInit - Claude Code Project Scaffolding Plugin

A Claude Code plugin that helps you quickly scaffold new projects with consistent coding guidelines and optional tooling setup.

## Features

- **Automated Guidelines Setup**: Automatically copies your global coding guidelines into each project's `CLAUDE.md`
- **Beads Integration**: Optional setup for Beads issue tracking with command whitelisting
- **Git Initialization**: Prompts to initialize git repositories when needed
- **Interactive Configuration**: Asks relevant questions to customize setup per project

## Installation

### Using Claude Code Plugin System

The easiest way to install this plugin is using the built-in plugin installer:

```
/plugin install <path-to-this-plugin>
```

For example, if you've cloned this repository to `~/claude-plugins/mfInit`:

```
/plugin install ~/claude-plugins/mfInit
```

Or install directly from a git repository:

```
/plugin install https://github.com/lacrioque/mfinit
```

After installation, the `/mf:init` command will be available in all your Claude Code sessions.

### Local Installation

1. Clone or copy this plugin to your local machine
2. In your Claude Code settings, add the plugin path to your configuration

### From npm (if published)

```bash
npm install -g @mf/init-plugin
```

## Usage

In any project directory, run:

```
/mf:init
```

The command will guide you through:

1. **Creating CLAUDE.md** - Copies your global coding guidelines into the project
2. **Beads Setup** (optional) - Initializes Beads issue tracking and offers to whitelist commands
3. **Git Initialization** (optional) - Creates a git repository if one doesn't exist

## What Gets Created

After running `/mf:init`, your project will have:

- **CLAUDE.md** - Your coding guidelines (based on GLOBAL_GUIDELINES.md)
- **.beads/** (optional) - Beads issue tracking directory
- **.git/** (optional) - Git repository

## Global Guidelines

The plugin uses the following coding standards (from GLOBAL_GUIDELINES.md):

1. English is our language
2. Names are important
3. Short, concise and functional
4. Single out classes
5. Documentation is king
6. Error reporting
7. Test for clarity
8. Clean Code principles
9. If and no else
10. Valuable documentation
11. Warm me of issues
12. Use Beads (optional - removed if you choose not to use Beads)

## Beads Command Whitelisting

If you choose to use Beads, the plugin will suggest whitelisting these commands in your Claude Code settings for convenience:

```
Bash(bd:*)
Bash(bd)
```

This allows Claude to run Beads commands without asking for permission each time.

## Customization

To customize the global guidelines:

1. Edit `GLOBAL_GUIDELINES.md` in the plugin directory
2. Your changes will be applied to all future projects initialized with `/mf:init`

## Requirements

- Claude Code CLI
- Beads (optional) - Install from [beads-marketplace](https://github.com/beyond-decentralized/beads)
- Git (optional)

## License

MIT

## Author

Created for consistent project scaffolding with Claude Code.
