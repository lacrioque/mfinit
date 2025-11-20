You are helping initialize a new project with proper guidelines and tooling.

Follow these steps in order:

1. **Add Global Guidelines**
   - Check if CLAUDE.md exists in the target project root
   - If it exists, read it first and append the guidelines below
   - If it doesn't exist, create it with the guidelines below
   - Add these Global Coding Guidelines to CLAUDE.md:

   ```
   # Global Coding Guidelines

   1. **English is our language** - Write everything in English, including identifiers, comments, commit messages, and documentation.
   2. **Names are important** - Use descriptive names for variables and methods that reveal intent.
   3. **Short, concise and functional** - Keep each function at approximately thirty lines or less and return early to reduce nesting.
   4. **Single out classes** - Place only one public class or component in a file.
   5. **Documentation is king** - Always add a docblock to every public symbol and focus on "why," not "what," in comments.
   6. **Error reporting** - Throw explicit errors instead of failing silently and log useful context such as operation, parameters, and identifiers.
   7. **Test for clarity** - Cover every public function with fast, deterministic unit tests.
   8. **Clean Code** - Apply the principles of Single Responsibility, Open/Closed, DRY, and YAGNI.
   9. **If and no else** - Use 'if' plenty, but avoid 'else' at all costs.
   10. **Valuable documentation** - Provide runnable examples and basic usage guidelines in global application documentation unless told otherwise.
   11. **Warn me of issues** - If any request conflicts with these English-plus-Clean-Code standards, reply with "Sorry, that conflicts with the English + Clean Code standard."
   12. **Use Beads** - Please use Beads to track and update your work exclusively.
   ```

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
- The target CLAUDE.md should be created/updated in the current working directory
- When appending to an existing CLAUDE.md, add a newline separator before adding the guidelines
