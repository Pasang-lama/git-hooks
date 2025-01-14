# What is git hooks?
Git hooks are scripts that Git executes automatically in response to specific events in a Git repository. They allow you to automate tasks, enforce policies, and customize your Git workflow.
Hooks are stored in the .git/hooks directory of a Git repository. They are typically written in shell scripting, but you can use any scripting language as long as the script is executable.

## Types of Git Hooks
### Git hooks are divided into two categories:

#### Client-Side Hooks: These are executed on operations like committing and merging. Examples:

* pre-commit: Runs before a commit is finalized, often used for linting, running tests, or formatting code.
* prepare-commit-msg: Used to modify the commit message before the editor is shown.
* commit-msg: Validates or modifies the commit message after the editor is closed.
* post-commit: Runs after a commit has been completed, often used for notifications or logging.

#### Server-Side Hooks: These are executed on a Git server during events like pushing or receiving changes. Examples:

* pre-receive: Runs before a push is accepted, often used to enforce access control or code quality checks.
* update: Runs before a specific branch is updated, used for branch-specific policies.
* post-receive: Runs after changes are pushed, often used for deploying code or notifying team members.
Enabling a Git Hook
Navigate to the .git/hooks directory in your repository.
Find the sample hook script (e.g., pre-commit.sample) and rename it by removing the .sample extension.
Edit the script and make it executable:
bash
  
1. chmod +x .git/hooks/pre-commit
