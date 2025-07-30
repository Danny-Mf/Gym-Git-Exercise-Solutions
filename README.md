# Gym-Git-Exercise-Solutions
## Bundle 1
### Exercises 1
```
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