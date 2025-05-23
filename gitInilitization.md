## Git Inilitization
- `git init` : Inilitize the repo.
    - This command create a hidden folder called `.git` which store all files to track the files and history.

- `git status` : Check for tracked and untracked files.
    - This command information about traked and untracked files in the git repository.
    - `Untracked` files are files that Git is not yet tracking.
    - `Tracked` file is a file that Git is tracking for changes.
    - For Git to track your files it should be in staging area.

- `git add [<file> <file>]` : For staging the files
    -`git add <file>` - Stage a file
    -`git add --all` or `git add -A` - Stage all changes

    - After staging the files you can check for the tracked files 
        -`git status` - See what is staged
        -`git restore --staged <file>` - Unstage a file

- `git commit -m "message"` : Commit snapshot the project
    - `commit` is save point of the project.
    - It records snapshot of files at a certain time, with a message describing what changed.
    - `git commit -m "message"` : Save your staged changes
    - `git commit -a -m "message"` : Automatically stage all tracked files that have been modified before committing but skip untracked/new files.

    ## More about commits in next commit :D
