# git-cafe-exercise

Bundle 5, Exercise 2
Below is the processing of cloning the forked project from the exercise and make changes while also creating a PR;
User@GisaF23 MINGW64 ~/Codes/project (main)
$ git clone https://github.com/Fuad-Jamal/git-cafe-exercise.git
Cloning into 'git-cafe-exercise'...
remote: Enumerating objects: 107, done.
remote: Counting objects: 100% (15/15), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 107 (delta 5), reused 4 (delta 4), pack-reused 92 (from 1)       
Receiving objects: 100% (107/107), 1.95 MiB | 1.43 MiB/s, done.
Resolving deltas: 100% (5/5), done.

User@GisaF23 MINGW64 ~/Codes/project (main)
$ cd git-cafe-exercise/

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)        
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git add index.html 

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git commit -m 'changed place to restaurant'
[main 8608e46] changed place to restaurant
 1 file changed, 1 insertion(+), 1 deletion(-)

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 328 bytes | 328.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Fuad-Jamal/git-cafe-exercise.git
   d1d3f9c..8608e46  main -> main

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git reset

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git revert
usage: git revert [--[no-]edit] [-n] [-m <parent-number>] [-s] [-S[<keyid>]] <commit>...
   or: git revert (--continue | --skip | --abort | --quit)

    --quit                end revert or cherry-pick sequence
    --continue            resume revert or cherry-pick sequence
    --abort               cancel revert or cherry-pick sequence
    --skip                skip current commit and continue
    --[no-]cleanup <mode> how to strip spaces and #comments from message       
    -n, --no-commit       don't automatically commit
    --commit              opposite of --no-commit
    -e, --[no-]edit       edit the commit message
    -s, --[no-]signoff    add a Signed-off-by trailer
    -m, --[no-]mainline <parent-number>
                          select mainline parent
    --[no-]rerere-autoupdate
                          update the index with reused conflict resolution if possible
    --[no-]strategy <strategy>
                          merge strategy
    -X, --[no-]strategy-option <option>
                          option for merge strategy
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG sign commit
    --[no-]reference      use the 'reference' format to refer to commits       


User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git log
commit 8608e4642d17112a9deee4c3f3cfc0533e958751 (HEAD -> main, origin/main, origin/HEAD)
Author: Fuad Jamal <jamalfuad34@gmail.com>
Date:   Thu May 22 17:14:22 2025 +0200

    changed place to restaurant

commit d1d3f9cb39e96d536a439a0bcb1206f073305b9b
Author: Yannick Musafiri <musayann@octangrp.com>
Date:   Thu Apr 7 19:39:24 2022 +0200

:
commit 8608e4642d17112a9deee4c3f3cfc0533e958751 (HEAD -> main, origin/main, origin/HEAD)
Author: Fuad Jamal <jamalfuad34@gmail.com>
Date:   Thu May 22 17:14:22 2025 +0200

    changed place to restaurant

commit d1d3f9cb39e96d536a439a0bcb1206f073305b9b
Author: Yannick Musafiri <musayann@octangrp.com>
Date:   Thu Apr 7 19:39:24 2022 +0200


User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git revert 8608e4642d17112a9deee4c3f3cfc0533e958751
hint: Waiting for your editor to close the file... Vim: Error reading input, exiting...
        Vim: preserving files...
Vim: Finished.
error: there was a problem with the editor 'vi'
Please supply the message using either -m or -F option.

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git revert 8608e4642d17112a9deee4c3f3cfc0533e958751
error: your local changes would be overwritten by revert.
hint: commit your changes or stash them to proceed.
fatal: revert failed

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index.html


User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git branch deve

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git branch
  deve
* main

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (main)
$ git checkout -d deve
M       index.html
HEAD is now at 8608e46 changed place to restaurant

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise ((8608e46...))
$ git branch
* (HEAD detached at refs/heads/deve)
  deve
  main

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise ((8608e46...))
$ git branch -d deve
Deleted branch deve (was 8608e46).

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise ((8608e46...))
$ git branch
* (HEAD detached at 8608e46)
  main

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise ((8608e46...))
$ git branch dev

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise ((8608e46...))
$ git checkout dev
M       index.html
Switched to branch 'dev'

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (dev)
$ git add index.html 

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (dev)
$ git commit -m 'changed restaurant from place in index'
On branch dev
nothing to commit, working tree clean

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (dev)
$ git pstatus
git: 'pstatus' is not a git command. See 'git --help'.

The most similar command is
        status

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (dev)
$ git status
On branch dev
nothing to commit, working tree clean

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (dev)
$ git status
On branch dev
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)        
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (dev)
$ git add index.html 

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (dev)
$ git commit -m 'changed place to restaurant'
[dev f1c8664] changed place to restaurant
 1 file changed, 1 insertion(+), 1 deletion(-)

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (dev)
$ git push --set-upstream origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 304 bytes | 304.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Fuad-Jamal/git-cafe-exercise/pull/new/dev      
remote:
To https://github.com/Fuad-Jamal/git-cafe-exercise.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.

User@GisaF23 MINGW64 ~/Codes/project/git-cafe-exercise (dev)
$
