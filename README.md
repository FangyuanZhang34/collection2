Collection
==========
<a href="#1">1. Git useful commands</a><br>
<a href="#2">2. Python useful packaging commands</a><br>
<br><br><br><br>

<a id="1"/><hr>
### 1. Git useful commands
##### update all branches from remote repository
```
git fetch
```
##### unstage add
```
git reset HEAD
```
##### unstage commit
```
git reset HEAD^
```
##### reset hard to a commit
```
git reset --hard <hash code>
```
##### reset hard to HEAD
```
git reset --hard HEAD
```
##### create and checkout a newbranch
```
git checkout -b newbranch
```
##### cherry-pick a commit from branch1 to branch2
```
git checkout branch1
git log
(copy the commit <hash code> you want to cherry-pick)
git checkout branch2
(stash or reset all the uncommitted changes in branch2)
git cherry-pick <hash code>
(the hash code will change after cherry-pick from branch1 to branch2)
```
<a href="#top">Back to top</a>

<a id="2"/><hr>
### 2. Python useful packaging commands
##### venv
Create a virtual environment for your application. It will have its own installation directories and doesn’t share libraries with other virtual environments.<br>
"Imagine you have an application that needs version 1 of LibFoo, but another application requires version 2. How can you use both these applications? If you install everything into /usr/lib/python3.6/site-packages (or whatever your platform’s standard location is), it’s easy to end up in a situation where you unintentionally upgrade an application that shouldn’t be upgraded."<br>
I choose to use venv, since it is available by default in Python 3.3 and later.
```
python3 -m venv <DIR>
source <DIR>/bin/activate
```
Then install any needed package versions for this specific application.<br>
https://pypi.org/<br>
When you want to deactivate the virtual environment, just type "deactivate".<br>
https://packaging.python.org/tutorials/installing-packages/<br>
https://docs.python.org/3/library/venv.html
##### pip
When using Python2.x, type 
```
python -m pip install <SomePackage>
```
when using Python3.x, type
```
python3 -m pip install <SomePackage>
```
<a href="#top">Back to top</a>
