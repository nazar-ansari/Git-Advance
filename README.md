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
git log -n 4                  (show last 4 commits)
git log -n 4 -p               (show last 4 commits in detail with addition & deletions)
git log Filename.txt          (show the commits which is related to Filename.txt)
git log --grep=<pattern>      (show commits that contains the message related to pattern)
```