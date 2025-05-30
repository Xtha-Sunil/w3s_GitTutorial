## Git Initialization & Basics

### 1. `git init` – Initialize the Repository
- Creates a hidden folder called `.git` that tracks changes and stores history for the project.

---

### 2. `git add` – Stage Files for Commit
- `git add <file>` – Stage a specific file.
- `git add --all` – Stage all changes (new, modified, deleted files).

**Check the status of staged/unstaged files:**
- `git status` – Show what's staged, modified, or untracked.
- `git restore --staged <file>` – Unstage a file.

---

### 3. `git status` – Show Current State
- Displays:
  - **Untracked files** – Not yet tracked by Git.
  - **Tracked files** – Being monitored by Git for changes.
- Files must be staged to be tracked and committed.

---

### 4. `git commit -m "message"` – Commit Snapshot of Project
- A commit is a save point capturing the current state of staged files.
- `git commit -m "message"` – Save staged changes with a message.
- `git commit -a -m "message"` – Automatically stage and commit all modified tracked files.
- `git commit` – Opens editor for writing a detailed message.

**Commit message guidelines:**
- Short summary under 50 characters.
- Use imperative mood (e.g., "Fix bug", not "Fixed bug").
- Leave one blank line before detailed description.

---

### 5. Other Useful Commit Options

1. **Create an empty commit (for marking purposes):**
   - `git commit --allow-empty -m "Start project"`

2. **Use previous commit message (skip editor):**
   - `git commit --no-edit`

3. **Amend the last commit (keep message):**
   - `git commit --amend --no-edit`

---

### 6. Troubleshooting Common Commit Mistakes

- **Forgot to stage a file?**
  - Run `git add <file>` and either:
    - Make a new commit, or
    - Use `git commit --amend` to add to the previous one.

- **Typo in your commit message?**
  - Use `git commit --amend -m "Corrected message"`.

- **Accidentally committed wrong files?**
  - Undo last commit and keep changes staged:
    - `git reset --soft HEAD~1`

---

### 7. View Commit History

- `git log` – View full commit history.
- `git log --oneline` – Condensed hash and message view.
- `git log --stat` – See stats about updated files.