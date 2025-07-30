# Gym-Git-Exercise-Solutions
## Bundle 1
### Exercises 1
``` bash
USER@Murengez MINGW64 ~/desktop (master)
$ mkdir gitExercises

USER@Murengez MINGW64 ~/desktop (master)
$ cd gitExercises

USER@Murengez MINGW64 ~/desktop/gitExercises (master)
$ git init
Initialized empty Git repository in C:/Users/USER/Desktop/gitExercises/.git/
USER@Murengez MINGW64 ~/desktop/gitExercises (master)
$ ls
index.html

USER@Murengez MINGW64 ~/desktop/gitExercises (master)
$ git branch -m main

USER@Murengez MINGW64 ~/desktop/gitExercises (main)
$ git add --all

USER@Murengez MINGW64 ~/desktop/gitExercises (main)
$ git commit -m"bundle 1 Exercise 1 midway attempt"
[main (root-commit) cf2c7f5] bundle 1 Exercise 1 midway attempt
 1 file changed, 9 insertions(+)
 create mode 100644 index.html

USER@Murengez MINGW64 ~/desktop/gitExercises (main)

USER@Murengez MINGW64 ~/desktop/gitExercises (main)
$ git checkout -b dev
Switched to a new branch 'dev'

USER@Murengez MINGW64 ~/desktop/gitExercises (dev)
$
$

USER@Murengez MINGW64 ~/desktop/gitExercises (main)
$ git checkout -b dev
Switched to a new branch 'dev'

USER@Murengez MINGW64 ~/desktop/gitExercises (dev)
$ git checkout -b test
Switched to a new branch 'test'

USER@Murengez MINGW64 ~/desktop/gitExercises (test)
$ git checkout dev
Switched to branch 'dev'

USER@Murengez MINGW64 ~/desktop/gitExercises (dev)

USER@Murengez MINGW64 ~/desktop/gitExercises (dev)
$ git branch -d test
Deleted branch test (was cf2c7f5).

```
### Exercise 2
``` bash

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ touch home.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git stash push -m"still working on home"
No local changes to save

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git stash push -m"still working on home"
No local changes to save

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git stash push -m"still working on home"
No local changes to save

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ ls
home.html  README.md

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git add home.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git stash push -m"still working on home"
Saved working directory and index state On dev: still working on home

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git stash list
stash@{0}: On dev: still working on home

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ touch about.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git add about.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ ls
about.html  README.md

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git stash push -m"still working on about"
Saved working directory and index state On dev: still working on about

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ touch team.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git add team.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ ls
README.md  team.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git stash push -m"still working on team"
Saved working directory and index state On dev: still working on team

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ ls
README.md

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git stash list
stash@{0}: On dev: still working on team
stash@{1}: On dev: still working on about
stash@{2}: On dev: still working on home

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (9b1862228e220d694f8e52c68442ee216f771ab8)   

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (f531821aae519b26b2e7049267e9d377db98b53f)   

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git commit -"home and about are now ready"
usage: git commit [-a | --interactive | --patch] [-s] [-v] [-u<mode>] [--amend]
                  [--dry-run] [(-c | -C | --squash) <commit> | --fixup [(amend|reword):]<commit>]
                  [-F <file> | -m <msg>] [--reset-author] [--allow-empty]
                  [--allow-empty-message] [--no-verify] [-e] [--author=<author>]
                  [--date=<date>] [--cleanup=<mode>] [--[no-]status]
                  [-i | -o] [--pathspec-from-file=<file> [--pathspec-file-nul]]
                  [(--trailer <token>[(=|:)<value>])...] [-S[<keyid>]]
                  [--] [<pathspec>...]

    -q, --[no-]quiet      suppress summary after successful commit
    -v, --[no-]verbose    show diff in commit message template 

Commit message options
    -F, --[no-]file <file>
                          read message from file
    --[no-]author <author>
                          override author for commit
    --[no-]date <date>    override date for commit
    -m, --[no-]message <message>
                          commit message
    -c, --[no-]reedit-message <commit>
                          reuse and edit message from specified commit
    -C, --[no-]reuse-message <commit>
                          reuse message from specified commit  
    --[no-]fixup [(amend|reword):]commit
                          use autosquash formatted message to fixup or amend/reword specified commit
    --[no-]squash <commit>
                          use autosquash formatted message to squash specified commit
    --[no-]reset-author   the commit is authored by me now (used with -C/-c/--amend)
    --trailer <trailer>   add custom trailer(s)
    -s, --[no-]signoff    add a Signed-off-by trailer
    -t, --[no-]template <file>
                          use specified template file
    -e, --[no-]edit       force edit of commit
    --[no-]cleanup <mode> how to strip spaces and #comments from message
    --[no-]status         include status in commit message template
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG sign commit

Commit contents options
    -a, --[no-]all        commit all changed files
    -i, --[no-]include    add specified files to index for commit
    --[no-]interactive    interactively add files
    -p, --[no-]patch      interactively add changes
    -o, --[no-]only       commit only specified files
    -n, --no-verify       bypass pre-commit and commit-msg hooks
    --verify              opposite of --no-verify
    --[no-]dry-run        show what would be committed
    --[no-]short          show status concisely
    --[no-]branch         show branch information
    --[no-]ahead-behind   compute full ahead/behind values     
    --[no-]porcelain      machine-readable output
    --[no-]long           show status in long format (default) 
    -z, --[no-]null       terminate entries with NUL
    --[no-]amend          amend previous commit
    --no-post-rewrite     bypass post-rewrite hook
    --post-rewrite        opposite of --no-post-rewrite        
    -u, --[no-]untracked-files[=<mode>]
                          show untracked files, optional modes: all, normal, no. (Default: all)
    --[no-]pathspec-from-file <file>
                          read pathspec from file
    --[no-]pathspec-file-nul
                          with --pathspec-from-file, pathspec elements are separated with NUL character


USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git commit -m"home and about are now ready"
[dev 7aeac20] home and about are now ready
 2 files changed, 29 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use 

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.     


USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 563 bytes | 563.00 KiB/s, done.   
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)  
remote: Resolving deltas: 100% (1/1), done.
remote:
remote: Create a pull request for 'dev' on GitHub by visiting: 
remote:      https://github.com/Danny-Mf/Bundle1/pull/new/dev  
remote:
To https://github.com/Danny-Mf/Bundle1.git
 * [new branch]      dev -> dev

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git push origin dev
Everything up-to-date

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git stash pop
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (55517fc72f3aafab6cc69c3448edd2e1837384e5)

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git reset HEAD team.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$

```