# Bundle 1
## exercise 1
```bash
PS C:\Users\alexa\Desktop\git_exercise> git init
Initialized empty Git repository in C:/Users/alexa/Desktop/git_exercise/.git/
PS C:\Users\alexa\Desktop\git_exercise> git add .\README.md
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "initial commit"
[master (root-commit) 21da833] initial commit
 1 file changed, 2 insertions(+)
 create mode 100644 README.md
PS C:\Users\alexa\Desktop\git_exercise> git status
On branch master
nothing to commit, working tree clean
PS C:\Users\alexa\Desktop\git_exercise> git branch -M main
PS C:\Users\alexa\Desktop\git_exercise> git remote add origin https://github.com/AL2002MI08/gym_git_exercises.git
PS C:\Users\alexa\Desktop\git_exercise> git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\alexa\Desktop\git_exercise> git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 242 bytes | 242.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/AL2002MI08/gym_git_exercises.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\alexa\Desktop\git_exercise> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\alexa\Desktop\git_exercise> git push dev
fatal: 'dev' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\alexa\Desktop\git_exercise> git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/AL2002MI08/gym_git_exercises/pull/new/dev
remote:
To https://github.com/AL2002MI08/gym_git_exercises.git
 * [new branch]      dev -> dev
PS C:\Users\alexa\Desktop\git_exercise> git status
On branch dev
nothing to commit, working tree clean
PS C:\Users\alexa\Desktop\git_exercise> git checkout -b test
Switched to a new branch 'test'
PS C:\Users\alexa\Desktop\git_exercise> git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/AL2002MI08/gym_git_exercises/pull/new/test
remote:
To https://github.com/AL2002MI08/gym_git_exercises.git
 * [new branch]      test -> test
PS C:\Users\alexa\Desktop\git_exercise> git checkout dev
Switched to branch 'dev'
PS C:\Users\alexa\Desktop\git_exercise> git branch -D test
Deleted branch test (was c6c7a32).
PS C:\Users\alexa\Desktop\git_exercise> git push --delete test
fatal: --delete doesn't make sense without any refs
PS C:\Users\alexa\Desktop\git_exercise> git push origin --delete test
To https://github.com/AL2002MI08/gym_git_exercises.git
 - [deleted]         test
```

## exercise 2
```bash
PS C:\Users\alexa\Desktop\git_exercise> git add .
PS C:\Users\alexa\Desktop\git_exercise> git status
        new file:   home.html
PS C:\Users\alexa\Desktop\git_exercise> git add .
PS C:\Users\alexa\Desktop\git_exercise> git status
        new file:   home.html
        new file:   about.html
PS C:\Users\alexa\Desktop\git_exercise> git stash 
Saved working directory and index state WIP on dev: 87a45e2 exercise 1 solution
PS C:\Users\alexa\Desktop\git_exercise> git add --all
PS C:\Users\alexa\Desktop\git_exercise> git stash
Saved working directory and index state WIP on dev: 87a45e2 exercise 1 solution
PS C:\Users\alexa\Desktop\git_exercise> git add --all
PS C:\Users\alexa\Desktop\git_exercise> git stash
Saved working directory and index state WIP on dev: 87a45e2 exercise 1 solution
PS C:\Users\alexa\Desktop\git_exercise> git stash list
stash@{0}: WIP on dev: 87a45e2 exercise 1 solution
stash@{1}: WIP on dev: 87a45e2 exercise 1 solution
stash@{2}: WIP on dev: 87a45e2 exercise 1 solution
PS C:\Users\alexa\Desktop\git_exercise> git stash pop 'stash@{1}'
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (2a5e47fb501dbff057b515b48fdc3d517c51d5d8)
PS C:\Users\alexa\Desktop\git_exercise> git stash show stash@{1}
Too many revisions specified: 'stash@' 'MQA=' 'xml' 'text'
PS C:\Users\alexa\Desktop\git_exercise> git stash list
stash@{0}: WIP on dev: 87a45e2 exercise 1 solution
stash@{1}: WIP on dev: 87a45e2 exercise 1 solution
PS C:\Users\alexa\Desktop\git_exercise> git stash pop 'stash@{1}'
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (40bb9fe6e6649ffe54036255d6d264baf7f70ab6)
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "added about and home page"
[dev 4f24dd1] added about and home page
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
PS C:\Users\alexa\Desktop\git_exercise> git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\alexa\Desktop\git_exercise> git push --set-upstream origin dev
Enumerating objects: 12, done.
Counting objects: 100% (12/12), done.
Delta compression using up to 12 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (10/10), 2.03 KiB | 691.00 KiB/s, done.
Total 10 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/AL2002MI08/gym_git_exercises.git
   c6c7a32..4f24dd1  dev -> dev
branch 'dev' set up to track 'origin/dev'.
PS C:\Users\alexa\Desktop\git_exercise> git stash pop 'stash@{0}'
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (6b4cc76f521bfe32f9d2752792cead647e131cc8)
PS C:\Users\alexa\Desktop\git_exercise> git reset --hard
HEAD is now at 4f24dd1 added about and home page
PS C:\Users\alexa\Desktop\git_exercise>
```
# bundle 4
## exercise 1
```bash
PS C:\Users\alexa\Desktop\git_exercise> git checkout main
error: Your local changes to the following files would be overwritten by checkout:
        README.md
Please commit your changes or stash them before you switch branches.
Aborting
PS C:\Users\alexa\Desktop\git_exercise> git add .
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "new changes to readme"
[ft/home-page-redesign 28ab819] new changes to readme
 1 file changed, 77 insertions(+)
PS C:\Users\alexa\Desktop\git_exercise> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\alexa\Desktop\git_exercise> git remote add git-copy https://github.com/AL2002MI08/gym_git_exercises_repo2.git
PS C:\Users\alexa\Desktop\git_exercise> git remote      
git-copy
origin
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "create new repo gitcopy"                                          
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\alexa\Desktop\git_exercise> git add .
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "create new repo gitcopy"
[main 7c13787] create new repo gitcopy
 1 file changed, 1 insertion(+)
PS C:\Users\alexa\Desktop\git_exercise> git push git-copy
Enumerating objects: 29, done.
Counting objects: 100% (29/29), done.
Delta compression using up to 12 threads
Compressing objects: 100% (24/24), done.
Writing objects: 100% (29/29), 5.24 KiB | 1.31 MiB/s, done.
Total 29 (delta 8), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (8/8), done.
To https://github.com/AL2002MI08/gym_git_exercises_repo2.git
 * [new branch]      main -> main
PS C:\Users\alexa\Desktop\git_exercise> git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 331 bytes | 331.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/AL2002MI08/gym_git_exercises.git
   42b575d..7c13787  main -> main
```

## exercise 2
```bash
PS C:\Users\alexa\Desktop\git_exercise> git add .
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "update readme"
[main 086a874] update readme
 1 file changed, 57 insertions(+), 2 deletions(-)
PS C:\Users\alexa\Desktop\git_exercise> git checkout -b ft/footer
Switched to a new branch 'ft/footer'
PS C:\Users\alexa\Desktop\git_exercise> git add .
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "add content to about page"
[ft/footer 476ccf5] add content to about page
 1 file changed, 1 insertion(+)
PS C:\Users\alexa\Desktop\git_exercise> git add .
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "add link to home page"
[ft/footer b28f834] add link to home page
 1 file changed, 1 insertion(+)
PS C:\Users\alexa\Desktop\git_exercise> git push
fatal: The current branch ft/footer has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/footer

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\alexa\Desktop\git_exercise> git push --set-upstream origin ft/footer
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 12 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 1.68 KiB | 245.00 KiB/s, done.
Total 9 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), completed with 3 local objects.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/AL2002MI08/gym_git_exercises/pull/new/ft/footer
remote:
To https://github.com/AL2002MI08/gym_git_exercises.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.
PS C:\Users\alexa\Desktop\git_exercise> git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
PS C:\Users\alexa\Desktop\git_exercise> git branch ft/squashing
PS C:\Users\alexa\Desktop\git_exercise> git checkout ft/squashing
Switched to branch 'ft/squashing'
PS C:\Users\alexa\Desktop\git_exercise> git merge squash ft/footer
merge: squash - not something we can merge
PS C:\Users\alexa\Desktop\git_exercise> git merge --squash ft/footer
Updating 086a874..b28f834
Fast-forward
Squash commit -- not updating HEAD
 about.html | 1 +
 home.html  | 1 +
 2 files changed, 2 insertions(+)
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "footer changes squashing"
[ft/squashing eedb323] footer changes squashing
 2 files changed, 2 insertions(+)
PS C:\Users\alexa\Desktop\git_exercise> git push origin ft/squashing
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 518 bytes | 259.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/AL2002MI08/gym_git_exercises/pull/new/ft/squashing
remote:
To https://github.com/AL2002MI08/gym_git_exercises.git
 * [new branch]      ft/squashing -> ft/squashing
PS C:\Users\alexa\Desktop\git_exercise> git push git-copy
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 12 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 1.57 KiB | 321.00 KiB/s, done.
Total 7 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/AL2002MI08/gym_git_exercises_repo2/pull/new/ft/squashing
remote:
To https://github.com/AL2002MI08/gym_git_exercises_repo2.git
 * [new branch]      ft/squashing -> ft/squashing
PS C:\Users\alexa\Desktop\git_exercise> git remote
git-copy
origin
PS C:\Users\alexa\Desktop\git_exercise> git push git-copy ft/squashing
Everything up-to-date
```