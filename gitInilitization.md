## Git Inilitization
1. `git init` : Inilitize the repo.
    - This command create a hidden folder called `.git` which store all files to track the files and history.

2. `git add [<file>]` : For staging the files
    -`git add <file>` - Stage a file
    -`git add --all`  - Stage all changes

    - After staging the files you can check for the tracked files 
        -`git status` - See what is staged
        -`git restore --staged <file>` - Unstage a file

3. `git status` : Check for tracked and untracked files.
    - Gives information about traked and untracked files in the git repository.
    - `Untracked` files are files that Git is not yet tracking.
    - `Tracked` file is a file that Git is tracking for changes.
    - For Git to track your files it should be in staging area.

4. `git commit -m "message"` : Commit snapshots the project.
    - `commit` is save point of the project.
    - It records snapshot of files at a certain time, with a message describing what changed.
    - `git commit -m "message"` : Save your staged changes
    - `git commit -a -m "message"` : Automatically stage all tracked files that have been modified before committing but skip untracked/new files.
    - `git commit` command will open default code editor, using this you can write multi-line comment.
        - Write short summary of commit (&lt; 50 chars)
        - Use imperative mood (eg. "Add feature" not "Added feature")
        - Leave 1 blank line
        - Write detail of comment.

5. Other Useful Commit Options
    1. Create an empty commit: `For marking`
        - git commit --allow-empty -m "Start project"
    2. Use previous commit message (no editor):
        - git commit --no-edit
    3. Quickly add staged changes to last commit, keep message:
        - git commit --amend --no-edit

6. Troubleshooting some common commit mistakes
    - Forgot to stage a file?
        - If you run git commit -m "message" but forgot to git add a file, just add it and commit again. Or use git commit --amend to add it to your last commit.
    - Typo in your commit message?
        - Use git commit --amend -m "Corrected message" to fix the last commit message.
    - Accidentally committed the wrong files?
        - You can use git reset --soft HEAD~1 to undo the last commit and keep your changes staged.

7. View commit history
    - `git log` : View history of repository
    - `git log --oneline` : View only condensed hash code and commit message
    - `git log --stat` : See stat about updated files