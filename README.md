<h1 align="center">🪄 <i>Advance Git-Concepts</i> 🪄</h1>
<div align="center"><img alt="Git-Image" src="https://icons.iconarchive.com/icons/papirus-team/papirus-apps/256/git-icon.png" ></div>
<hr>

**_Cloning a Repo with specific Templates_**
```python
git clone --template=../Example/* https://github.com/example/Repo.git
```
**_Cloning a Repo with specific No of Commits (Clone till last 5 COMMITS)_**
```python
git clone --depth=5 https://github.com/example/Repo.git
```
**_Cloning a specific Branch of Reop_**
```python
git clone --branch=feature https://github.com/example/Repo.git
```
**_Configuring Colors_**
```python
(black,red,green,yellow,blue,magenta,cyan,white)

git config --(global|local|system) color.ui true

git config --(global|local|system) color.branch.current "yellow"    (sets current branch color)

git config --(global|local|system) color.branch.local "cyan"        (sets local branch color)

git config --(global|local|system) color.branch.remote "white"      (sets remote branch color)

git config --(global|local|system) color.branch.upstream "magenta"   (sets Upstream branch color)

git config --(global|local|system) color.grep.match "white"        (sets matching text in `git log --grep=<pattern>` color)

git config --(global|local|system) color.diff.new "yellow"        (sets color for new changes while git diff)

git config --(global|local|system) color.diff.old "red"           (sets color for old changes while git diff)
```
**_Configuring Default editor for everything while newcommits or rebasing n all_**
```python
git config --global core.editor "code -w"       (Default editorto VScode)

git config --global core.editor "notepad.exe"       (Default editor to notepad )

git config --global core.editor "nano -w"       (Default editor to nano )

git config --global core.editor "vim"       (Default editor to vim )
```
**_Configuring Alias for ease of access_**
```python
git config --global alias.unstage 'reset --hard HEAD '
git unstage
```
**_Configuring Users and Emails_**
```python
git config --global user.name "Alex Christopher"
git config --global user.email "alex@christopher"
git config --global --add user.name "Shezam kroker"
git config --global --add user.email "shezam@kroker"
```
**_While Commiting_**
```python
git commit -am "YOUR SAMPLE MESSAGE"      (add first and then commit)
git commit --amend -m "rewrite the previous message at HEAD"    (rewrite the past commit message)
git commit --amend --no-edit       (add the changes and use the previous commit)
git commit --amend --no-edit --author="Derek Cause <derek@cause>"
```
**_Getting Differences_**
```python
git diff --staged         (see changes after staging the working directory)
git diff main..develop Sample.txt   (show differences what is in develop & not in main branch of `Sample.txt` file)
git diff --color-words      (show changes what is added and deleted in better way)
```
**_Stashing Changes_**
```python
git stash                     (stashes only staged or the one which was commited earlier{file})
git stash -u                  (stash both staged changes and the File/Folder Created FirstTime)
git stash -a                  (all even inclue file which are ignored)
git stash save "Unique Message"         (save this stash with name "Unique Message")
git stash list -n 3           (show last three stashes)
git stash show stash@{0} -p   (show the changes in this stash with detail changes )
git stash pop                 (apply back recent stash to working directory)
git stash apply stash@{1}     (apply back copy of recent stash and keep original in stash )
git stash drop                (drop the recent stash)
git stash clear               (clear all the stashes)
git stash branch feature stash@{0}      (apply stash changes to new branch)
```
**_Setting Custom .gitignore File_**
```python
git config --global core.excludesFile ~/.gitignore
```
**_Listing Logs of Commits_**
```python
git log -n 4                                      (show last 4 commits)
git log -n 4 -p                                   (show last 4 commits in detail with addition & deletions)
git log Filename.txt                              (show the commits which is related to Filename.txt)
git log --grep=<pattern>                          (show commits that contains the message related to pattern)
git log --graph --oneline --decorate              (shows the logs in graph related to the branches with single line commits)
git log --before=01-02-2022 --after=25-01-2022    (shows the commits between range of dates)
git log --oneline BranchA..BranchB                (commits which are present in BranchB & not in BranchA)
```
**_Tags in Commits_**
```python
git tag -a V1.1 -m "Initial Release"
git tag -a V1.2 -m "Second Release" HEAD~2
git tag -a V1.2 -m "Third Release" HEAD~2 -f
git checkout V1.1            (to Checkout to Specific Tag as a Detached HEAD)
git push origin --tags       (by Default normal pushing doesn't push tags on Repo need to use `--tags` )
git tag -d V1.1              (to delete specific tag)
```
**_Inspecting a Specific File with Blame_**
```python
git blame index.html      (show the recent changes done by whom and what was changes)
git blame -e index.html   (show the email instead of name)
git blame -w index.html   (ignore the commits that consists any whitespace changes by other author)
```
**_Cleaning a Folder&Files That are created First Time_**
```python
git clean -n -x -d -f     (-n:DRY test , -x:inclued ignored one , -d: Directory , -f:force)
git rm -rf {File/FolderName}
```
**_Reverting a Specific Commit_**
```python
git revert {commitID_No}              (inverse the changes to specific commit in working directory)
git revert --no-edit {commitID_No}    (inverse the changes but do not open editor for reverting message)
git revert -n {commitID_No}           (inverse the changes but do not commit)
```
**_Resetting the working directory and checkouts_**
```python
git reset index.html                (unstage the file)
git reset HEAD~2                    (move head to specific commit and leave changes further from it in Working Directory)
git reset --hard HEAD~2             (move head to specific commit Strictly without leaving and further changes)
git reset --hard remote/BranchA     (force to match the commits as per the remote log's)
```
**_Restoring Changes_**
```python
git restore Filename                (restore the working changes to HEAD)
git restore --staged Filename       (restore the changes from Staging area to Working Directory)
git restore --source=HEAD~2 .       (restore all changes in working directory to HEAD~2)
git restore -p Filename             (restore only specific HUNK of changes {y/n})
```
**_Remote URL's config_**
```python
git remote -v                                       (show all remotes)
git remote add origin https://github.com/example    (add remote name origin)
git remote get-url origin                           (displays the url of remote)
git remote set-url origin                           (change past url address to another address)
git remote rename origin Another_name               (change name of remote)
git remote show origin                              (show detail Information about Specific Origin)
```