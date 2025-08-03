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
## Bundle #2
### Exercise #1
```bash 

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git branch ft/bundle-2

USER@Murengez MINGW64 ~/Desktop/Bundle1 (dev)
$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/bundle-2)
$ touch service.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/bundle-2)
$ git add service.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/bundle-2)
$ ls
about.html  home.html  README.md  service.html  team.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/bundle-2)
$ git commit -m"added service page"
[ft/bundle-2 97e71e7] added service page
 1 file changed, 16 insertions(+)
 create mode 100644 service.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/bundle-2)
$ git branch
  dev
* ft/bundle-2
  main

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/bundle-2)
$ git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/bundle-2)
$ git push --set-upstream ft/bundle-2
fatal: 'ft/bundle-2' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/bundle-2)
$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 450 bytes | 450.00 KiB/s, done.   
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)  
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Danny-Mf/Bundle1/pull/new/ft/bundle-2
remote:
To https://github.com/Danny-Mf/Bundle1.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/bundle-2)
$ 1

```
## Exercise #2\
```bash

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/bundle-2)
$ git checkout main
M       service.html
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

USER@Murengez MINGW64 ~/Desktop/Bundle1 (main)
$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 914 bytes | 130.00 KiB/s, done.
From https://github.com/Danny-Mf/Bundle1
   95ebb44..2ef7a9d  main       -> origin/main
Updating 97e71e7..2ef7a9d
Fast-forward

USER@Murengez MINGW64 ~/Desktop/Bundle1 (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/service-redesign)  
$ git add .

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/service-redesign)  
$ git commit -m "added new changes to the service page"
[ft/service-redesign 5acae51] added new changes to the service page
 2 files changed, 13 insertions(+), 2 deletions(-)
 create mode 100644 team.html

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/service-redesign)  
$ git push
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/service-redesign)
$
GNU bash, version 5.2.37(1)-release (x86_64-pc-msys)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 542 bytes | 542.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Danny-Mf/Bundle1/pull/new/ft/service-redesign
remote:
To https://github.com/Danny-Mf/Bundle1.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/service-redesign)  
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

USER@Murengez MINGW64 ~/Desktop/Bundle1 (main)
$ git add .

USER@Murengez MINGW64 ~/Desktop/Bundle1 (main)
$ git push
Everything up-to-date

USER@Murengez MINGW64 ~/Desktop/Bundle1 (main)
$ git push origin main
Everything up-to-date

USER@Murengez MINGW64 ~/Desktop/Bundle1 (main)
$ git commit -m "added services"
[main 6cffceb] added services
 1 file changed, 6 insertions(+)

USER@Murengez MINGW64 ~/Desktop/Bundle1 (main)
$ git add .

USER@Murengez MINGW64 ~/Desktop/Bundle1 (main)
$ git commit -m "changed the title"
[main 63d4088] changed the title
 1 file changed, 1 insertion(+), 1 deletion(-)

USER@Murengez MINGW64 ~/Desktop/Bundle1 (main)
$ git push 
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 748 bytes | 748.00 KiB/s, done.   
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)  
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
To https://github.com/Danny-Mf/Bundle1.git
   2ef7a9d..63d4088  main -> main

USER@Murengez MINGW64 ~/Desktop/Bundle1 (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.   

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/service-redesign)  
$ git diff ft/service-redesign main
diff --git a/service.html b/service.html
index 0252777..bd8ac2b 100644
--- a/service.html
+++ b/service.html
@@ -4,12 +4,18 @@
 <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=], initial-scale=1.0">
-    <title>ft | Service page</title>
+    <title>service</title>
 </head>

 <body>
     <div>
-        <p>Services</p>
+        <p>ServicesS</p>
+        <ul>
+            <li>Web design</li>
+            <li>CCTV Camera installation</li>
+            <li>Arduino Programming</li>
+            <li>Mutugane pp</li>
+        </ul>
     </div>
 </body>

diff --git a/team.html b/team.html
deleted file mode 100644
index 7488b49..0000000
--- a/team.html
+++ /dev/null


CONFLICT (content): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/service-redesign|MERGING)
$ git add .

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/service-redesign|MERGING)
$ git commit -m "ft/service-redesign and main are now merged\"
> 
> 
> git commit -m "ft/service-redesign and main are now merged\"

fatal: cannot do a partial commit during a merge.

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/service-redesign|MERGING)
$ git add .

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/service-redesign|MERGING)
$ git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)


USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/service-redesign|MERGING)
$ git commit
[ft/service-redesign 1bdb089] Merge branch 'main' into ft/service-redesign

USER@Murengez MINGW64 ~/Desktop/Bundle1 (ft/service-redesign)
$ git push
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 241 bytes | 241.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Danny-Mf/Bundle1.git
   5acae51..1bdb089  ft/service-redesign -> ft/service-redesign

```
# Bundle #3
## Exercise #1
```bash
62  git branch ft/team-page
   63  git checkout ft/team-page
   64  touch team.html
   65  git add --all
   66  git commit -m "added team page"
   67  git push --upstream-origin ft/team-page       
   68  git push
   69  git push --set-upstream origin ft/team-page   
   70  git checkout main
   71  git branch ft/contact-page
   72  git checkout ft/team-page
   73  git log
   74  git checkout ft/contact-page
   75  git cherry-pick 957f992a5cefbaa698fb4c2e599da4bc3c0b3fc2
   76  touch contact.html
   77  git add .
   78  git commit -m "added contact page"
   79  git push --set-upstream origin ft/contact-page
   80  git branch checkout -b ft/faq-page
   81  git branch checkout -b "ft/faq-page"
   82  git checkout -b "ft/faq-page"
   83  touch faq.html
   84  git add .
   85  git commmit -m "added faq page"
   86  git commit -m "added faq page"
   87  git push --set-upstream origin ft/faq-page    
   88  git revert 957f992a5cefbaa698fb4c2e599da4bc3c0b3fc2
   89  git log
   90  git push --set-uptream origin ft/faq-page     
   91  git push --set-upstream origin ft/faq-page    
  

   ```
   ## Exercise #2
   ```bash 

51  git checkout ft/faq-page
   52  git branch ft/home-page-redesign
   53  git checkout main
   54  touch service.html
   55  git add .
   56  git commit origin main
   57  git commit -m"added service page"
   58  git push origin main
   59  git pull
   60  git push
   61  git checkout ft/home-page-redesign
   62  git rebase main
   63  git add .
   64  git commit -m"added title to the home page"   
   65  git push --set-upstream origin ft/home-page-redesign

   ```
   # Bundle #4
   ## Exercise #1
   ```bash
    git checkout main
   76  git add remote git-copy https://github.com/Danny-Mf/bundle4-Repo.git
   77  git remote add git-copy https://github.com/Danny-Mf/bundle4-Repo.git
   78  git add .
   79  git commit -m "added p to the home page"
   80  git push
   81  git reset HEAD~
   82  git status
   83  git add .
   84  git commit -m "added p to the home page"
   85  git push origin git-copy
   86  git remote -v
   87  git remote
   88  git push origin
   89  git push
   90  git pull
   91  git push origin
   92  git push git-copy
   93  git pull
   94  git remote
   95  git push git-copy
   96  git pull
   97  git push
   98  git push git-copy
   99  git reset HEAD~
  100  git status
  101  git push
  102  git pull
  103  git push git copy
  104  git push git-copy
  105  git pull
  106  git add
  107  git add --all
  108  git commit -m "added p to the home page"
  109  git push origin
  110  git push git-copy
  112  git push git-copy main --force
   ```

   ## Exercise 2
   ```bash
    git checkout -b ft/footer
  116  touch footer.html
  117  git add .
  118  git commit -m "added footer page"
  119  git add .
  120  git commit -m "added social media Icon"
  121  git push --set-upstream ft/footer
  122  git push
  123  git push --set-upstream origin ft/footer
  124  git checkout main
  125  git checkout  ft/footer
  126  git reset HEAD~
  127  git add .
  128  git commit -m "added social media Icon"
  129  git push --set-upstream origin ft/footer
  130  git pull
  131  git push --set-upstream origin ft/footer
  132  git add .
  133  git commit -m "added social media list"
  134  git push --set-upstream origin ft/footer
  135  git checkout main
  136  git branch ft/squashing
  137  git merge squash ft/footer
  138  git checkout -b ft/squash
  139  git merge squash ft/footer
  140  git merge --squash ft/footer
  141  git add .
  142  git commit -m "footer changes  squashing"
  143  git push --set-upstream origin ft/squash
   ```

   # Bundle #5 
   ## Exercise #1 and #2
   ```bash
   git add index.html
   52  git commit -m "changed the main title"
   53  git push
   ```
   ## Bundle 6
   ```bash
   51  git status
   52  git checkout -b feature
   53  touch menu.html
   54  git add menu.html
   55  git commit -m "Added menu page"
   56  git push --set-upstream origin feature
   57  git checkout -b bug fix
   58  git checkout -b "bug-fix"
   59  git add index-4.html
   60  git status
   61  git commit -m "index-4.html | Changed title for Menu to Contacts"
   62  git push --set-upstream origin bug-fix
   63  git add index-4.html
   64  git commit -m "index-4.html | Changed Contact to +1 800 659 6035"
   65  git push --set-upstream origin bug-fix
   ```
