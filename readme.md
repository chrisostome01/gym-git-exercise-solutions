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








