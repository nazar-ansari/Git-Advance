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