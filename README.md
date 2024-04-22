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

# Bundle 2
## exercise 1 and exercise 2
```bash
PS C:\Users\alexa\Desktop\git_exercise> git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
PS C:\Users\alexa\Desktop\git_exercise> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\alexa\Desktop\git_exercise> git branch     
  dev
  ft/bundle-2
* main
PS C:\Users\alexa\Desktop\git_exercise> git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'
PS C:\Users\alexa\Desktop\git_exercise> git add .
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "added service page"
[ft/bundle-2 d9ca2b5] added service page
 1 file changed, 15 insertions(+)
 create mode 100644 services.html
PS C:\Users\alexa\Desktop\git_exercise> git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\alexa\Desktop\git_exercise> git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 483 bytes | 483.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/AL2002MI08/gym_git_exercises/pull/new/ft/bundle-2
remote:
To https://github.com/AL2002MI08/gym_git_exercises.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
PS C:\Users\alexa\Desktop\git_exercise> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\alexa\Desktop\git_exercise> git pull
Already up to date.
PS C:\Users\alexa\Desktop\git_exercise> git pull origin main
From https://github.com/AL2002MI08/gym_git_exercises
 * branch            main       -> FETCH_HEAD
Already up to date.
PS C:\Users\alexa\Desktop\git_exercise> git add .
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "merged files"
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\alexa\Desktop\git_exercise> git push origin main
To https://github.com/AL2002MI08/gym_git_exercises.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/AL2002MI08/gym_git_exercises.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS C:\Users\alexa\Desktop\git_exercise> git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 907 bytes | 302.00 KiB/s, done.
From https://github.com/AL2002MI08/gym_git_exercises
   c6c7a32..f2d6658  main       -> origin/main
Updating c6c7a32..f2d6658
Fast-forward
 README.md     | 118 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 about.html    |  12 ++++++
 home.html     |  12 ++++++
 services.html |  15 ++++++++
 4 files changed, 157 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html
PS C:\Users\alexa\Desktop\git_exercise> git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
PS C:\Users\alexa\Desktop\git_exercise> git add .
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "added div"
[ft/service-redesign b54e96d] added div
 1 file changed, 3 insertions(+)
PS C:\Users\alexa\Desktop\git_exercise> git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\alexa\Desktop\git_exercise>  git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 619 bytes | 619.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/AL2002MI08/gym_git_exercises/pull/new/ft/service-redesign
remote:
To https://github.com/AL2002MI08/gym_git_exercises.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
PS C:\Users\alexa\Desktop\git_exercise> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\alexa\Desktop\git_exercise> git add .
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "add new content to service page"
[main 42b575d] add new content to service page
 1 file changed, 1 insertion(+)
PS C:\Users\alexa\Desktop\git_exercise> git push  
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 601 bytes | 601.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/AL2002MI08/gym_git_exercises.git
   f2d6658..42b575d  main -> main
PS C:\Users\alexa\Desktop\git_exercise> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
PS C:\Users\alexa\Desktop\git_exercise> git diff main
diff --git a/services.html b/services.html
index 4e69a02..f9363f3 100644
--- a/services.html
+++ b/services.html
@@ -11,6 +11,8 @@
         <li>car washing</li>
         <li>party hosting</li>
     </ul>
-    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem consequatur quia consectetur error distinctio numquam, possimus, assumenda commodi unde dolorum illum corrupti non natus vero animi porro velit sequi nulla?</p>
+    <div class="description">
+       <span><p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Porro assumenda cupiditate, tenetur saepe corporis, eligendi nisi doloribus cum placeat eos reiciendis incidunt nemo aliquam ex nesciunt itaque, aliquid illo dolorum.</p></span>
+    </div>
 </body>
 </html>
\ No newline at end of file
PS C:\Users\alexa\Desktop\git_exercise> git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
PS C:\Users\alexa\Desktop\git_exercise> git merge main
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
PS C:\Users\alexa\Desktop\git_exercise> git add .\services.html
PS C:\Users\alexa\Desktop\git_exercise> git commit -m "add changes services page"
[ft/service-redesign e26bb23] add changes services page
PS C:\Users\alexa\Desktop\git_exercise> git commit --amend -m "add changes and feature branch"
[ft/service-redesign 82e850c] add changes and feature branch
 Date: Mon Apr 22 16:07:39 2024 +0200
PS C:\Users\alexa\Desktop\git_exercise> git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 505 bytes | 505.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/AL2002MI08/gym_git_exercises.git
   b54e96d..82e850c  ft/service-redesign -> ft/service-redesign
```