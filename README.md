# Git Exercises

## Bundle 1

### Exercise 1

```bash
DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
        new file:   index.html
        new file:   styles.css

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (master)
$ git branch -m master main

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
        new file:   index.html
        new file:   styles.css

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html
        modified:   styles.css

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (main)
$ git commit -m "Add styles.css and heading title to the html file"
[main (root-commit) 3dba784] Add styles.css and heading title to the html file
 3 files changed, 9 insertions(+)
 create mode 100644 README.md
 create mode 100644 index.html
 create mode 100644 styles.css

$ git push -u origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (7/7), 1.16 KiB | 10.00 KiB/s, done.
Total 7 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/ishimweClaude12/Gym-Git-Exercise-Solutions.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (main)
$ git log --oneline
2e21de9 (HEAD -> main, origin/main) Add README File
3dba784 Add styles.css and heading title to the html file
 #### Creating dev and test branches
 DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (main)
$ git branch dev

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (main)
$ git branch
  dev
* main

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (main)
$ git checkout dev
Switched to branch 'dev'
M       index.html
M       styles.css

### Deleting Test Branch
DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (main)
$ git branch -d test
Deleted branch test (was 2e21de9).

## Bundle 1   Exercise 2
DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (main)
$ git branch
  dev
* main

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (main)
$ git branch dev
fatal: a branch named 'dev' already exists

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (main)
$ git checkout dev
Switched to branch 'dev'

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git add home.html

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git stash list

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html


DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git stash
Saved working directory and index state WIP on dev: 2e21de9 Add README File

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git stash list
stash@{0}: WIP on dev: 2e21de9 Add README File

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git add about.html

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git stash
Saved working directory and index state WIP on dev: 2e21de9 Add README File

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git add team.html

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git stash
Saved working directory and index state WIP on dev: 2e21de9 Add README File

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git stash list
stash@{0}: WIP on dev: 2e21de9 Add README File
stash@{1}: WIP on dev: 2e21de9 Add README File
stash@{2}: WIP on dev: 2e21de9 Add README File

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (8fa976ce0a2d3c22b522352baf81c6b50a3fd95e)

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git stash pop
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   team.html

Dropped refs/stash@{0} (86ae686d224c32dc772ed136529bda0ae1e78400)

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git stash pop
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
        new file:   team.html

Dropped refs/stash@{0} (130e67ba57e050c3ae090c6855dea9ef162ac2db)

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git commit -m "Add Home, About and Team pages"
[dev 6c8e42a] Add Home, About and Team pages
 3 files changed, 30 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 team.html

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git stash list

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git log --onelist
fatal: unrecognized argument: --onelist

DAVTECH LTD@Claude MINGW64 ~/Desktop/GitExercises (dev)
$ git log --oneline
6c8e42a (HEAD -> dev) Add Home, About and Team pages
2e21de9 Add README File
3dba784 Add styles.css and heading title to the html file
```
