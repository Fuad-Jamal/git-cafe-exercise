# git-cafe-exercise
Bundle 6, Exercise 1
Below is the work done based on the instructions to complete this exercise;
User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git checkout -b feature
Switched to a new branch 'feature'

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (feature)
$ git add index-3
fatal: pathspec 'index-3' did not match any files

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (feature)
$ git add index-3.html 

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (feature)
$ git commit -m 
error: switch `m' requires a value

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (feature)
$ git commit -m ' updating menu'
[feature d20f71d]  updating menu
 1 file changed, 1 insertion(+), 1 deletion(-)

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (feature)
$ git push
fatal: The current branch feature has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin feature

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (feature)
$ git push --set-upstream origin feature
To https://github.com/Fuad-Jamal/git-cafe-exercise.git
 ! [rejected]        feature -> feature (non-fast-forward)
error: failed to push some refs to 'https://github.com/Fuad-Jamal/git-cafe-exercise.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,     
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.     

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (feature)
$ git push --set-upstream origin feature
To https://github.com/Fuad-Jamal/git-cafe-exercise.git
 ! [rejected]        feature -> feature (non-fast-forward)
error: failed to push some refs to 'https://github.com/Fuad-Jamal/git-cafe-exercise.git'
hint: Updates were rejected because the tip of your current branch is behind   
hint: its remote counterpart. If you want to integrate the remote changes,     
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.     

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (feature)
$ git branch -m ft/feature

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (ft/feature)
$ git branch
  dev
* ft/feature
  main

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (ft/feature)
$ git push
fatal: The current branch ft/feature has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/feature

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (ft/feature)
$ git push --set-upstream orgin ft/feature 
fatal: 'orgin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (ft/feature)
$ git status
On branch ft/feature
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)        
        modified:   index-4.html

no changes added to commit (use "git add" and/or "git commit -a")

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (ft/feature)
$ git add index-4.html 

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (ft/feature)
$ git commit -m 'updating menu'
[ft/feature 36661a1] updating menu
 1 file changed, 1 insertion(+), 1 deletion(-)

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (ft/feature)
$ git push
fatal: The current branch ft/feature has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/feature

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (ft/feature)
$ git push --set-upstream orgin ft/feature 
fatal: 'orgin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (ft/feature)
$ git push --set-upstream origin ft/feature
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 594 bytes | 594.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 3 local objects.
remote:
remote: Create a pull request for 'ft/feature' on GitHub by visiting:
remote:      https://github.com/Fuad-Jamal/git-cafe-exercise/pull/new/ft/feature
remote:
To https://github.com/Fuad-Jamal/git-cafe-exercise.git
 * [new branch]      ft/feature -> ft/feature
branch 'ft/feature' set up to track 'origin/ft/feature'.