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

git config --(global|local|system) color.branch.current "yellow"    (sets current branch color)

git config --(global|local|system) color.branch.local "cyan"        (sets local branch color)

git config --(global|local|system) color.branch.remote "white"        (sets remote branch color)

git config --(global|local|system) color.branch.upstream "magenta"        (sets Upstream branch color)
```