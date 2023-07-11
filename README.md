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


```
