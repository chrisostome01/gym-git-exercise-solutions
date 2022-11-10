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


### Exercises 2

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








## Bundle 3


### Exercises 1


```bash

    
 ~/Desktop/gitEx/bandle (main)
$ git branch
  dev
  ft/bundle-2
  ft/service-redesign
* main

 ~/Desktop/gitEx/bandle (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

 ~/Desktop/gitEx/bandle (ft/team-page)
$ git add .

 ~/Desktop/gitEx/bandle (ft/team-page)
$ git commit -m "feat: adds team page" 
[ft/team-page ea2c7a3] feat: adds team page
 1 file changed, 12 insertions(+)
 create mode 100644 team.html

 ~/Desktop/gitEx/bandle (ft/team-page)
$ git push -u origin ft/team-page
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
 ! [rejected]        ft/team-page -> ft/team-page (non-fast-forward)
error: failed to push some refs to 'https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

 ~/Desktop/gitEx/bandle (ft/team-page)
$

 ~/Desktop/gitEx/bandle (ft/team-page)
$ git push -u origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 488 bytes | 244.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions/pull/new/ft/team-page
remote:
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

 ~/Desktop/gitEx/bandle (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

 ~/Desktop/gitEx/bandle (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git log
commit 569a4fb5ea524484a1eab722cf9ca4139059b8f3 (HEAD -> ft/contact-page, origin/main, main)
Author: sezerano jean chrysostome <sezeranochrisostom123@gmail.com>
Date:   Thu Nov 10 14:02:56 2022 +0200

    feat: adds service changes on main

commit e73abf7e0eba1b7e86dfbe09b5a7693389cf495a
Merge: afa927e 60c0a2d
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Thu Nov 10 13:36:35 2022 +0200

    Merge pull request #1 from sezeranoJchrisostome/ft/bundle-2

    #GIT Exercises bandle2 #1

commit 60c0a2d8c3480320e88b055aa00503ec4104d642 (origin/ft/bundle-2, ft/bundle-2)
Author: sezerano jean chrysostome <sezeranochrisostom123@gmail.com>

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git checkout ft/team-page 
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

 ~/Desktop/gitEx/bandle (ft/team-page)
$ git log
commit ea2c7a36ed9a08cfe41ba90d64b97df95a831f02 (HEAD -> ft/team-page, origin/ft/team-page)
Author: sezerano jean chrysostome <sezeranochrisostom123@gmail.com>
Date:   Thu Nov 10 15:55:54 2022 +0200

    feat: adds team page

commit 569a4fb5ea524484a1eab722cf9ca4139059b8f3 (origin/main, main, ft/contact-page)
Author: sezerano jean chrysostome <sezeranochrisostom123@gmail.com>
Date:   Thu Nov 10 14:02:56 2022 +0200

    feat: adds service changes on main

commit e73abf7e0eba1b7e86dfbe09b5a7693389cf495a
Merge: afa927e 60c0a2d
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Thu Nov 10 13:36:35 2022 +0200


 ~/Desktop/gitEx/bandle (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git cherry-pick ea2c7a36ed9a08cfe41ba90d64b97df95a831f021~
fatal: bad revision 'ea2c7a36ed9a08cfe41ba90d64b97df95a831f021~'

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git cherry-pick ea2c7a36ed9a08cfe41ba90d64b97df95a831f021
fatal: bad revision 'ea2c7a36ed9a08cfe41ba90d64b97df95a831f021'

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git fetch origin 

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git cherry-pick ea2c7a36ed9a08cfe41ba90d64b97df95a831f021
fatal: bad revision 'ea2c7a36ed9a08cfe41ba90d64b97df95a831f021'

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git cherry-pick ea2c7a36ed9a08cfe41ba90d64b97df95a831f021
fatal: bad revision 'ea2c7a36ed9a08cfe41ba90d64b97df95a831f021'

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git checkout ea2c7a36ed9a08cfe41ba90d64b97df95a831f021~
error: pathspec 'ea2c7a36ed9a08cfe41ba90d64b97df95a831f021~' did not match any file(s) known to git

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git checkout ea2c7a36ed9a08cfe41ba90d64b97df95a831f021
error: pathspec 'ea2c7a36ed9a08cfe41ba90d64b97df95a831f021' did not match any file(s) known to git

 ~/Desktop/gitEx/bandle (ft/contact-page)
$

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git cherry-pick ea2c7a36ed9a08cfe41ba90d64b97df95a831f021~
fatal: bad revision 'ea2c7a36ed9a08cfe41ba90d64b97df95a831f021~'

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git cherry-pick ea2c7a36ed9a08cfe41ba90d64b97df95a831f021
fatal: bad revision 'ea2c7a36ed9a08cfe41ba90d64b97df95a831f021'

 ~/Desktop/gitEx/bandle (ft/contact-page)
$


 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git cherry-pick ea2c7a36ed9a08cfe41ba90d64b97df95a831f02
[ft/contact-page fabc0ba] feat: adds team page
 Date: Thu Nov 10 15:55:54 2022 +0200
 1 file changed, 12 insertions(+)
 create mode 100644 team.html

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git status
On branch ft/contact-page
nothing to commit, working tree clean

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git push -u origin ft/contact-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 490 bytes | 490.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions/
pull/new/ft/contact-page
remote:
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.



 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git add .

 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git commit -m "feat: add faq page"
[ft/faq-page 2e640b2] feat: add faq page
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html

 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git push -u origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 483 bytes | 241.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions/pull/new/ft/faq-page
remote:
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

 ~/Desktop/gitEx/bandle (ft/faq-page)
$



 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git log
commit 2e640b24f3d34ba26b1bcc6de6c127bedca49bc2 (HEAD -> ft/faq-page, origin/ft/
faq-page)
Author: sezerano jean chrysostome <sezeranochrisostom123@gmail.com>
Date:   Thu Nov 10 16:39:41 2022 +0200

    feat: add faq page

commit fabc0ba89a51b1bbd8a08981623d1d9da677dc21 (origin/ft/contact-page, ft/cont
act-page)
Author: sezerano jean chrysostome <sezeranochrisostom123@gmail.com>
Date:   Thu Nov 10 15:55:54 2022 +0200

    feat: adds team page

commit 569a4fb5ea524484a1eab722cf9ca4139059b8f3 (origin/main, main)
Author: sezerano jean chrysostome <sezeranochrisostom123@gmail.com>
Date:   Thu Nov 10 14:02:56 2022 +0200

    feat: adds service changes on main

commit e73abf7e0eba1b7e86dfbe09b5a7693389cf495a
Merge: afa927e 60c0a2d
Author: Chrissie <chrissiemhrk@gmail.com>

 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

 ~/Desktop/gitEx/bandle (ft/team-page)
$ git log
commit ea2c7a36ed9a08cfe41ba90d64b97df95a831f02 (HEAD -> ft/team-page, origin/ft
/team-page)
Author: sezerano jean chrysostome <sezeranochrisostom123@gmail.com>
Date:   Thu Nov 10 15:55:54 2022 +0200

    feat: adds team page

commit 569a4fb5ea524484a1eab722cf9ca4139059b8f3 (origin/main, main)
Author: sezerano jean chrysostome <sezeranochrisostom123@gmail.com>
Date:   Thu Nov 10 14:02:56 2022 +0200

    feat: adds service changes on main
Revert "feat: adds team page"























[ft/faq-page 084914a] Revert "feat: adds team page"
 1 file changed, 12 deletions(-)
 delete mode 100644 team.html

 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git push -u origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 287 bytes | 287.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
   2e640b2..084914a  ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

 ~/Desktop/gitEx/bandle (ft/faq-page)



```








### Exercises 2

```bash

 ~/Desktop/gitEx/bandle (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git add .

 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git commit -m "feat: add faq page"
[ft/faq-page 2e640b2] feat: add faq page
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html

 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git push -u origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 483 bytes | 241.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions/pull/new/ft/faq-page
remote:
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git add .

 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git commit -m "feat: submit bundle 3 exercise one"
[ft/faq-page 3856f7e] feat: submit bundle 3 exercise one
 1 file changed, 328 insertions(+)

 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git push -u origin ft/faq-page
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 3.02 KiB | 1.51 MiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
   084914a..3856f7e  ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git chekcout -b ft/home-page-redesign
git: 'chekcout' is not a git command. See 'git --help'.

The most similar command is
        checkout

 ~/Desktop/gitEx/bandle (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git checkout main 
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

 ~/Desktop/gitEx/bandle (main)
$ git add .

 ~/Desktop/gitEx/bandle (main)
$ git commit -m "feat: redesign home page"
[main 0d1f8f1] feat: redesign home page
 1 file changed, 1 insertion(+), 1 deletion(-)

 ~/Desktop/gitEx/bandle (main)
$ git push -u origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 326 bytes | 326.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
   569a4fb..0d1f8f1  main -> main
branch 'main' set up to track 'origin/main'.

 ~/Desktop/gitEx/bandle (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git rebase main 
Successfully rebased and updated refs/heads/ft/home-page-redesign.

 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git puhs -u origin ft/home-page-redesign
git: 'puhs' is not a git command. See 'git --help'.

The most similar command is
        push

 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git push -u origin ft/home-page-redesign
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 4 threads
Compressing objects: 100% (11/11), done.
Writing objects: 100% (11/11), 3.97 KiB | 677.00 KiB/s, done.
Total 11 (delta 5), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (5/5), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions/pull/new/ft/home-page-redesign
remote:
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git add .

 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git commit -m "feat: adds some new changes"
[ft/home-page-redesign d0f21b1] feat: adds some new changes
 1 file changed, 1 insertion(+)

 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git push -u origin ft/home-page-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 360 bytes | 360.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/sezeranoJchrisostome/gym-git-exercise-solutions.git
   e5db5fd..d0f21b1  ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

 ~/Desktop/gitEx/bandle (ft/home-page-redesign)

```








## Bundle 4


### Exercises 1


```bash


 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git add .

 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git commit -m "feat: submit bundle 3 exercise2"
[ft/home-page-redesign 3f6ddb2] feat: submit bundle 3 exercise2
 1 file changed, 148 insertions(+)

 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
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

 ~/Desktop/gitEx/bandle (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

 ~/Desktop/gitEx/bandle (main)
$  git remote add git-copy https://github.com/sezeranoJchrisostome/git-exercise-clone.git

 ~/Desktop/gitEx/bandle (main)
$ git add .

 ~/Desktop/gitEx/bandle (main)
$ git commit -m "feat: redesign home.html for two repo"
[main 8a6fe7e] feat: redesign home.html for two repo
 1 file changed, 2 insertions(+), 1 deletion(-)

 ~/Desktop/gitEx/bandle (main)
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

 ~/Desktop/gitEx/bandle (main)
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


 ~/Desktop/gitEx/bandle (main)
$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'

 ~/Desktop/gitEx/bandle (ft/footer)
$ gi add .
bash: gi: command not found

 ~/Desktop/gitEx/bandle (ft/footer)
$  git add .

 ~/Desktop/gitEx/bandle (ft/footer)
$ git commit -m "feat: add footer page"
[ft/footer 17edc03] feat: add footer page
 1 file changed, 14 insertions(+)
 create mode 100644 footer.html

 ~/Desktop/gitEx/bandle (ft/footer)
$ git add .

 ~/Desktop/gitEx/bandle (ft/footer)
$  git commit -m "feat: adds more footer content"
[ft/footer e7ae6cb] feat: adds more footer content
 1 file changed, 3 insertions(+), 1 deletion(-)

 ~/Desktop/gitEx/bandle (ft/footer)
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

 ~/Desktop/gitEx/bandle (ft/footer)
$ git checkout main 
Switched to branch 'main'
Your branch is up to date with 'git-copy/main'.

 ~/Desktop/gitEx/bandle (main)
$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'

 ~/Desktop/gitEx/bandle (ft/squashing)
$ git merge squash ft/footer
merge: squash - not something we can merge

 ~/Desktop/gitEx/bandle (ft/squashing)
$ git merge --squash ft/footer
Updating 8a6fe7e..e7ae6cb
Fast-forward
Squash commit -- not updating HEAD
 footer.html | 16 ++++++++++++++++
 1 file changed, 16 insertions(+)
 create mode 100644 footer.html

 ~/Desktop/gitEx/bandle (ft/squashing)
$ git status
On branch ft/squashing
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   footer.html


 ~/Desktop/gitEx/bandle (ft/squashing)
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

 ~/Desktop/gitEx/bandle (ft/squashing)
$ git restore .

 ~/Desktop/gitEx/bandle (ft/squashing)
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

 ~/Desktop/gitEx/bandle (ft/squashing)
$ git commit -m "footer changes squashing"
[ft/squashing 4694a87] footer changes squashing
 1 file changed, 16 insertions(+)
 create mode 100644 footer.html

 ~/Desktop/gitEx/bandle (ft/squashing)
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

 ~/Desktop/gitEx/bandle (ft/squashing)
$


```


