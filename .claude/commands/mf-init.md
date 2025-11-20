You are helping initialize a new project with proper guidelines and tooling.

Follow these steps in order:

1. **Copy Global Guidelines**
   - Read the GLOBAL_GUIDELINES.md file from the plugin directory
   - Create or update CLAUDE.md in the target project root
   - Copy the entire contents of GLOBAL_GUIDELINES.md into CLAUDE.md

2. **Ask about Beads**
   - Use AskUserQuestion to ask: "Would you like to use Beads for issue tracking in this project?"
   - If YES:
     - Run `bd init` using the Bash tool
     - Use AskUserQuestion to ask: "Would you like to whitelist Bash(bd:*) and Bash(bd) commands for convenience? This allows Claude to run beads commands without asking for permission each time."
     - If the user agrees, inform them to add the following to their Claude Code settings:
       ```
       Bash(bd:*)
       Bash(bd)
       ```
   - If NO: Edit the CLAUDE.md file to remove Rule 12 (the "Use Beads" rule)

3. **Check Git Repository**
   - Check if the current directory is already a git repository
   - If NOT a git repo:
     - Use AskUserQuestion to ask: "This directory is not a git repository. Would you like to initialize one?"
     - If YES: Run `git init` using the Bash tool

4. **Completion**
   - Confirm to the user that the project has been initialized
   - List what was set up (CLAUDE.md created, beads initialized if applicable, git initialized if applicable)

Important notes:
- Always use the AskUserQuestion tool for user prompts
- Use the Bash tool for running commands
- The GLOBAL_GUIDELINES.md file should be in the plugin's root directory
- The target CLAUDE.md should be created in the current working directory
