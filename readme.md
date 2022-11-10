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
