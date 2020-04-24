# README #
This file as well was created without creating a repo online on github

## 1. Steps local:
- Do not worry if you have multiple local commmits already(Skip Step 1)
- Create project directory folder
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
- Commit command: `git commit -m "first local commit"`

## 2. Steps Github(or any git tool):
- Github does not have option to create a new repo from cli before installing some kind of other tool (as per last I know)
- So first create a new repo on Github(I named it `local-folder-to-github` same as my local folder name)
- Didn't selected the option to create a readme as I alreadt created one here
- Time to connect this local folder to online repo
- Copy repo url from github(in my case: `https://github.com/abhi5658/local-folder-to-github.git`)
- Now got to cli and add remote to this local repo:
    - Git command: `git remote add origin repo_url` (e.g. `git remote add origin https://github.com/abhi5658/local-folder-to-github.git`)
- Check if this is connected now git command: `git remote -v`
    - shows the fetch and push remote urls
- You can try pushing the local commits but that would fail as first you need to pull remote commits
- Time to pull the remote commits to local repo:
    - Git commmand: `git pull origin master`
    - produces error: 'fatal: refusing to merge unrelated histories'
    - By pass this error by git command: `git pull origin master --allow-unrelated-histories`
    - This would merge the local commits with the pulled commits(initial commit)
- Push local commits to remote repo:
    - Git command: `git push origin master`
- Now the local commits and whole local folder(also a git repository) is pushed to online(remote) repository.