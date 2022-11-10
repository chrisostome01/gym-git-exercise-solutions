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


### Exercises 1

```bash


 ~/Desktop/gitEx/bandle (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

 ~/Desktop/gitEx/bandle (main)
$ git pull orgin main 
fatal: 'orgin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

 ~/Desktop/gitEx/bandle (main)
$ git pull origin main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 638 bytes | 106.00 KiB/s, done.
From https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions
 * branch            main       -> FETCH_HEAD
   afa927e..e73abf7  main       -> origin/main
Updating afa927e..e73abf7
Fast-forward
 about.html   |  12 +++
 home.html    |  12 +++
 readme.md    | 320 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 service.html |  12 +++
 4 files changed, 355 insertions(+), 1 deletion(-)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 service.html

 ~/Desktop/gitEx/bandle (main)
$ git checkout -b ft/service-redesign
fatal: a branch named 'ft/service-redesign' already exists

 ~/Desktop/gitEx/bandle (main)
$ git branch -D ft/service-redesign
Deleted branch ft/service-redesign (was cce0df3).

 ~/Desktop/gitEx/bandle (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

 ~/Desktop/gitEx/bandle (ft/service-redesign)
$ git add .

 ~/Desktop/gitEx/bandle (ft/service-redesign)
$ git commit -m "feat: add new content to service page"
[ft/service-redesign 5fe82f6] feat: add new content to service page
 1 file changed, 1 insertion(+), 1 deletion(-)


 ~/Desktop/gitEx/bandle (ft/service-redesign)
$ git pull origin ft/service-redesign
From https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions
 * branch            ft/service-redesign -> FETCH_HEAD
Auto-merging service.html
CONFLICT (add/add): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.

 ~/Desktop/gitEx/bandle (ft/service-redesign|MERGING)
$ git merge --abort


 ~/Desktop/gitEx/bandle (ft/service-redesign)
$ git pull origin ft/service-redesign --rebase
From https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions
 * branch            ft/service-redesign -> FETCH_HEAD
Auto-merging service.html
CONFLICT (add/add): Merge conflict in service.html
error: could not apply 526286f... feat: adds service page
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
Could not apply 526286f... feat: adds service page


 ~/Desktop/gitEx/bandle (ft/service-redesign|REBASE 4/6)
$ git rebase --continue 
Successfully rebased and updated refs/heads/ft/service-redesign.

 ~/Desktop/gitEx/bandle (ft/service-redesign)
$ git push -u origin ft/service-redesign
Enumerating objects: 22, done.
Counting objects: 100% (22/22), done.
Delta compression using up to 4 threads
Compressing objects: 100% (19/19), done.
Writing objects: 100% (19/19), 3.34 KiB | 855.00 KiB/s, done.
Total 19 (delta 10), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (10/10), done.
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
   cce0df3..b5d1d9c  ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.



 ~/Desktop/gitEx/bandle (main)
$ git add .

 ~/Desktop/gitEx/bandle (main)
$ git commit -m "feat: adds service changes on main"
[main 569a4fb] feat: adds service changes on main
 1 file changed, 1 insertion(+), 1 deletion(-)

 ~/Desktop/gitEx/bandle (main)
$ git push -u origin main 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 329 bytes | 329.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
   e73abf7..569a4fb  main -> main
branch 'main' set up to track 'origin/main'.



 ~/Desktop/gitEx/bandle (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

 ~/Desktop/gitEx/bandle (ft/service-redesign)
$ git diff main
diff --git a/service.html b/service.html
index 2b96ddf..14dcc89 100644
--- a/service.html
+++ b/service.html
@@ -7,6 +7,6 @@
     <title>Service</title>
 </head>
 <body>
-    <h1> Hello am service page , main changes </h1>    
+    <h1> Hello am service page , new changes </h1>    
 </body>
 </html>
\ No newline at end of file

 ~/Desktop/gitEx/bandle (ft/service-redesign)
$ git merge main
Auto-merging service.html
CONFLICT (add/add): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.

 ~/Desktop/gitEx/bandle (ft/service-redesign|MERGING)
$ git add .

 ~/Desktop/gitEx/bandle (ft/service-redesign|MERGING)
$ git commit -m "fix: resolve conflict"
[ft/service-redesign 9935ed1] fix: resolve conflict

 ~/Desktop/gitEx/bandle (ft/service-redesign)
$ git push -u origin ft/service-redesign
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 233 bytes | 233.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
   b5d1d9c..9935ed1  ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

 ~/Desktop/gitEx/bandle (ft/service-redesign)



```