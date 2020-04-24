# README #
This file as well was created without creating a repo online on github

## Steps:
- Create preoject directory folder
- Create files/folders/anything inside it
- Now this folder is still not a git repo(that tracks changes)
- Open git bash to the parent directory(as per basics)
- First thing initialise it with git command: `git init`
- `.git` (may be hidden) folder is created which will now track the changes now in this directory
- set user name and user email for this directory if it is different from the global user
- Check credential using git command: `git config -l`
    - If it shows user.name and user.email set to the credential you want then nothing to do.
    - If not set name and email using using git command: 
        - `git config user.name "Your name"`
        - `git config user.email "emailid@thatcompany.com"`
    - Check again if the new credentials(if different) appears at end of list commmand: `git config -l`
- Check status of tracked files command: `git status`
- Add files to track. Easiest command: `git add --all`
- Now time to commit this much