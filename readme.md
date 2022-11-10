# GIT Exercises

## Bundle 1


### Exercises 1


```bash 

~/Desktop/gitEx/bandle
$ git init 
Initialized empty Git repository in C:/Users/TheGym/Desktop/gitEx/bandle/.git/

~/Desktop/gitEx/bandle (master)
$ git branch -M master main


 ~/Desktop/gitEx/bandle (main)
$ git add .

~/Desktop/gitEx/bandle (main)
$ git commit -m "feat: add readme file "
[main (root-commit) afa927e] feat: add readme file
 1 file changed, 11 insertions(+)
 create mode 100644 readme.md

 ~/Desktop/gitEx/bandle (main)
$ git remote add origin https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git

 ~/Desktop/gitEx/bandle (main)
$ git push -u origin main 
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.    
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done. 
Writing objects: 100% (3/3), 276 bytes | 92.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

~/Desktop/gitEx/bandle (main)
$ git checkout -b dev
Switched to a new branch 'dev'

 ~/Desktop/gitEx/bandle (dev)
$ git checkout test 
error: pathspec 'test' did not match any file(s) known to git

 ~/Desktop/gitEx/bandle (dev)
$ git checkout -b test
Switched to a new branch 'test'

 ~/Desktop/gitEx/bandle (test)
$ git checkout dev
Switched to branch 'dev'

~/Desktop/gitEx/bandle (dev)
$ git branch -D test 
Deleted branch test (was afa927e).

 ~/Desktop/gitEx/bandle (dev)
$ git branch
* dev
  main


```




### Exercises 2


```bash 

~/Desktop/gitEx/bandle 
(dev)
$ git add .


 ~/Desktop/gitEx/bandle 
(dev)
$ git stash -m "home stash"
Saved working directory and index state On dev: home stash

~/Desktop/gitEx/bandle 
(dev)
$ git add .

 ~/Desktop/gitEx/bandle 
(dev)
$ git stash -m "about page stash"
Saved working directory and index state On dev: about 
page stash

 ~/Desktop/gitEx/bandle 
(dev)
$ git add .


~/Desktop/gitEx/bandle 
(dev)
$ git stash -m "team page stash"
Saved working directory and index state On dev: team page stash



~/Desktop/gitEx/bandle 
(dev)
$ git stash list
stash@{0}: On dev: team page stash
stash@{1}: On dev: about page stash
stash@{2}: On dev: home stash

~/Desktop/gitEx/bandle  
(dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)   
        new file:   about.html

Dropped stash@{1} (d038f9a2cd59533469d285b0cdd0ee4f65fa6d66)

~/Desktop/gitEx/bandle 
(dev)
$ git stash list
stash@{0}: On dev: team page stash
stash@{1}: On dev: home stash

~/Desktop/gitEx/bandle 
(dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)   
        new file:   about.html


~/Desktop/gitEx/bandle 
(dev)
$ git add .

 ~/Desktop/gitEx/bandle 
(dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)   
        new file:   about.html

~/Desktop/gitEx/bandle 
(dev)
$ git stash list 
stash@{0}: On dev: team page stash
stash@{1}: On dev: home stash

 ~/Desktop/gitEx/bandle 
(dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)   
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (b8cca76977019bedf7efc3ae99165d97c48e5d88)


~/Desktop/gitEx/bandle 
(dev)
$ git add .


~/Desktop/gitEx/bandle 
(dev)
$ git commit -m "feat: adds home and about page"
[dev e7c7dad] feat: adds home and about page
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

 ~/Desktop/gitEx/bandle 
(dev)
$ git push -u origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 566 bytes | 283.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0  
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
   3dd19fd..e7c7dad  dev -> dev
branch 'dev' set up to track 'origin/dev'.


 ~/Desktop/gitEx/bandle 
(dev)
$ git stash list 
stash@{0}: On dev: team page stash

 ~/Desktop/gitEx/bandle 
(dev)
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)   
        new file:   team.html

Dropped stash@{0} (f9db812a77a36b54f7e9face7ff302cda6752f5a)

 ~/Desktop/gitEx/bandle 
(dev)
$ git reset --hard
HEAD is now at e7c7dad feat: adds home and about page


```
