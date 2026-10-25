# CLAUDE.md

## Git Rules

- Use `GitHub Flow` as the branching strategy
  - main / feature
- Use `Conventional Commits` for commit messages
- Use the gh command for GitHub operations

## Git Worktree Rules

- Do implementation work in a worktree under `<repo>/.claude/worktrees/<name>/` (`claude -w <name>` / EnterWorktree)
  - Keep the main checkout clean for the user's own work and reviews
  - Small fixes, investigation, and questions can be done in the current directory
- One task = one worktree = one branch = one PR
  - Name the worktree after the branch (e.g. `feat-xxx`)
- Copy gitignored files such as `.env` via `.worktreeinclude`; install dependencies in each worktree
- Do not run tasks that touch the same files in parallel worktrees
- Remove the worktree after the PR is merged (`git worktree remove` / `git worktree prune`)
