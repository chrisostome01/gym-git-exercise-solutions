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

## Bundle 2


### Exercises 1


```bash

 ~/Desktop/gitEx/bandle 
(dev)                                                 (dev)
$ git commit -m "feat: submit second exercise on bandle one"
[dev 2dcf7b9] feat: submit second exercise on bandle one
 1 file changed, 163 insertions(+)                    ne

 ~/Desktop/gitEx/bandle 
(dev)                                                 (dev)
$ git push -u origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.46 KiB | 746.00 KiB/s, done.
done.                                                      
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0   local object.
remote: Resolving deltas: 100% (1/1), completed with 1rcise-solutions.git local object.
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
   e7c7dad..2dcf7b9  dev -> dev                       (dev)
branch 'dev' set up to track 'origin/dev'.


 ~/Desktop/gitEx/bandle 
(dev)
$ git chekcout -b ft/bundle-2
git: 'chekcout' is not a git command. See 'git --help'.

The most similar command is
        checkout


 ~/Desktop/gitEx/bandle 
(dev)
$ git chekckout -b ft/bundle-2
git: 'chekckout' is not a git command. See 'git --help'.

The most similar command is
        checkout


 ~/Desktop/gitEx/bandle 
(dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'


 ~/Desktop/gitEx/bandle 
(ft/bundle-2)
$ git add .



 ~/Desktop/gitEx/bandle 
(ft/bundle-2)
$ git commit -m "feat: adds service page"
[ft/bundle-2 526286f] feat: adds service page
 1 file changed, 12 insertions(+)
 create mode 100644 service.html



 ~/Desktop/gitEx/bandle 
(ft/bundle-2)
$ git push -u origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 495 bytes | 247.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions/pull/new/ft/bundle-2        
remote:
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.



 ~/Desktop/gitEx/bandle
(ft/bundle-2)
$


```


## Bundle 4


### Exercises 1


```bash


 MINGW64 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git add .

 MINGW64 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git commit -m "feat: submit bundle 3 exercise2"
[ft/home-page-redesign 3f6ddb2] feat: submit bundle 3 exercise2
 1 file changed, 148 insertions(+)

 MINGW64 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git push -u origin ft/home-page-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Writing objects: 100% (3/3), 1.05 KiB | 538.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
   d0f21b1..3f6ddb2  ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

 MINGW64 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

 MINGW64 ~/Desktop/gitEx/bandle (main)
$  git remote add git-copy https://github.com/sezeranoJchrisostome/git-exercise-clone.git

 MINGW64 ~/Desktop/gitEx/bandle (main)
$ git add .

 MINGW64 ~/Desktop/gitEx/bandle (main)
$ git commit -m "feat: redesign home.html for two repo"
[main 8a6fe7e] feat: redesign home.html for two repo
 1 file changed, 2 insertions(+), 1 deletion(-)

 MINGW64 ~/Desktop/gitEx/bandle (main)
$ git push -u origin main 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 378 bytes | 94.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
   0d1f8f1..8a6fe7e  main -> main
branch 'main' set up to track 'origin/main'.

 MINGW64 ~/Desktop/gitEx/bandle (main)
$ git push -u git-copy main
Enumerating objects: 29, done.
Counting objects: 100% (29/29), done.
Delta compression using up to 4 threads
Compressing objects: 100% (27/27), done.
Writing objects: 100% (29/29), 4.69 KiB | 686.00 KiB/s, done.
Total 29 (delta 14), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (14/14), done.
To https://github.com/sezeranoJchrisostome/git-exercise-clone.git
 * [new branch]      main -> main
branch 'main' set up to track 'git-copy/main'.

```


### Exercises 2


```bash


 MINGW64 ~/Desktop/gitEx/bandle (main)
$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'

 MINGW64 ~/Desktop/gitEx/bandle (ft/footer)
$ gi add .
bash: gi: command not found

 MINGW64 ~/Desktop/gitEx/bandle (ft/footer)
$  git add .

 MINGW64 ~/Desktop/gitEx/bandle (ft/footer)
$ git commit -m "feat: add footer page"
[ft/footer 17edc03] feat: add footer page
 1 file changed, 14 insertions(+)
 create mode 100644 footer.html

 MINGW64 ~/Desktop/gitEx/bandle (ft/footer)
$ git add .

 MINGW64 ~/Desktop/gitEx/bandle (ft/footer)
$  git commit -m "feat: adds more footer content"
[ft/footer e7ae6cb] feat: adds more footer content
 1 file changed, 3 insertions(+), 1 deletion(-)

 MINGW64 ~/Desktop/gitEx/bandle (ft/footer)
$ git push -u origin ft/footer
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 787 bytes | 393.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions/pull/new/ft/footer
remote:
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.

 MINGW64 ~/Desktop/gitEx/bandle (ft/footer)
$ git checkout main 
Switched to branch 'main'
Your branch is up to date with 'git-copy/main'.

 MINGW64 ~/Desktop/gitEx/bandle (main)
$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'

 MINGW64 ~/Desktop/gitEx/bandle (ft/squashing)
$ git merge squash ft/footer
merge: squash - not something we can merge

 MINGW64 ~/Desktop/gitEx/bandle (ft/squashing)
$ git merge --squash ft/footer
Updating 8a6fe7e..e7ae6cb
Fast-forward
Squash commit -- not updating HEAD
 footer.html | 16 ++++++++++++++++
 1 file changed, 16 insertions(+)
 create mode 100644 footer.html

 MINGW64 ~/Desktop/gitEx/bandle (ft/squashing)
$ git status
On branch ft/squashing
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   footer.html


 MINGW64 ~/Desktop/gitEx/bandle (ft/squashing)
$ restore
usage: restore [OPTIONS] [PATTERN [PATTERN...]]
Options are:

   -a, --all               Restore all filesystems.
   -l, --level=LEVEL       Start restoring from the given backup LEVEL
                           (default 0).
   -v, --verbose[=LEVEL]   Set verbosity level. Default 100.

Informational options:
   -h, --help              Display this help message.
   -V, --version           Display program version.

Send bug reports to bug-tar@gnu.org.

 MINGW64 ~/Desktop/gitEx/bandle (ft/squashing)
$ git restore .

 MINGW64 ~/Desktop/gitEx/bandle (ft/squashing)
$ git log 
commit 8a6fe7e4e5c72cdfac9eb7ef96c2c3535e8b6951 (HEAD -> ft/squashing, origin/main, git-copy/main, main)
Author: sezerano jean chrysostome <sezeranochrisostom123@gmail.com>
Date:   Thu Nov 10 17:36:27 2022 +0200

    feat: redesign home.html for two repo

commit 0d1f8f154f7bc362df0fd490f923e601834ec713
Author: sezerano jean chrysostome <sezeranochrisostom123@gmail.com>
Date:   Thu Nov 10 17:02:16 2022 +0200

    feat: redesign home page

commit 569a4fb5ea524484a1eab722cf9ca4139059b8f3
Author: sezerano jean chrysostome <sezeranochrisostom123@gmail.com>
Date:   Thu Nov 10 14:02:56 2022 +0200

    feat: adds service changes on main

 MINGW64 ~/Desktop/gitEx/bandle (ft/squashing)
$ git commit -m "footer changes squashing"
[ft/squashing 4694a87] footer changes squashing
 1 file changed, 16 insertions(+)
 create mode 100644 footer.html

 MINGW64 ~/Desktop/gitEx/bandle (ft/squashing)
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 495 bytes | 247.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions/pull/new/ft/squashing
remote:
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.

 MINGW64 ~/Desktop/gitEx/bandle (ft/squashing)
$


```

