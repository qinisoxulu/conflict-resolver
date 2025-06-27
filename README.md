
# conflict-resolver

A shell script that automates Git conflict resolution and smooths out the push process for large teams working on a shared codebase.

## Key Features

- Detects uncommitted local changes and safely stashes them.
- Fetches the latest changes from the remote branch.
- Creates a backup branch before rebasing.
- Rebases changes onto the latest main branch.
- Automatically resolves merge conflicts using the "ours" strategy.
- Pushes changes, with `--force-with-lease` fallback for safety.
- Restores stashed changes after successful push.

## Usage

Download: `conflict-resolver.sh` to the home of your project.

Make the script executable:

```bash
chmod +x conflict-resolver.sh
```



### Sample Workflow

1. Developer pulls the latest code.
2. Makes changes to the folder and runs `git add .` + `git commit -m "SOme commit"` instead of a manual `git push`.
3. The script automatically handles conflict resolution and pushing every minute after you commit.
`DO NOT RUN 'git push' IF YOU ARE USING THIS SCRIPT`

## Screenshots

![conflict-resolver workflow](assets/conflict-resolver-diagram.png)

## 🧪 Requirements

- Git installed
- Linux/macOS terminal
- Sufficient permission to push to the remote repository

## Warnings

- This script auto-resolves conflicts using the "ours" strategy, which **keeps your local version** and discards remote conflicting changes.
- Recommended only for workflows where you are sure your version is the desired resolution.
- Use with caution and always ensure proper backup/version control.

## License

MIT License

---

Happy coding!