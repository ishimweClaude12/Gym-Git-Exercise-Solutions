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



User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/bundle-2)olutions (ft/bundle-2)
$ git branch ft/team-page

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git branch
* ft/bundle-2
  ft/service-redesign
  ft/team-page
  main

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git switch ft/team-page
Switched to branch 'ft/team-page'

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git add .

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git commit -m 'Add new team members'
[ft/team-page b201290] Add new team members
 1 file changed, 3 insertions(+)

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push --set-upstream origin ft/team-page~
fatal: invalid refspec 'ft/team-page~'

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git status
On branch ft/team-page
nothing to commit, working tree clean

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push --set-upstream origin ft/team-page~
fatal: invalid refspec 'ft/team-page~'

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 353 bytes | 353.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/ishimweClaude12/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/ishimweClaude12/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git switch ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log
commit b2012903df6981db5e2569ca7d606b39b772ee8c (HEAD -> ft/team-page, origin/ft/team-page)
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Tue Jul 25 10:41:41 2023 +0200

    Add new team members


User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git stash --list
error: unknown option `list'
usage: git stash list [<log-options>]
   or: git stash show [-u | --include-untracked | --only-untracked] [<diff-options>] [<stash>]
   or: git stash drop [-q | --quiet] [<stash>]
   or: git stash pop [--index] [-q | --quiet] [<stash>]
   or: git stash apply [--index] [-q | --quiet] [<stash>]
   or: git stash branch <branchname> [<stash>]
   or: git stash [push [-p | --patch] [-S | --staged] [-k | --[no-]keep-index] [-q | --quiet]
                 [-u | --include-untracked] [-a | --all] [(-m |
--message) <message>]
                 [--pathspec-from-file=<file> [--pathspec-file-nul]]
                 [--] [<pathspec>...]]
   or: git stash save [-p | --patch] [-S | --staged] [-k | --[no-]keep-index] [-q | --quiet]
                 [-u | --include-untracked] [-a | --all] [<message>]
   or: git stash clear
   or: git stash create [<message>]
   or: git stash store [(-m | --message) <message>] [-q | --quiet] <commit>

    -k, --keep-index      keep index
    -S, --staged          stash staged changes only
    -p, --patch           stash in patch mode
    -q, --quiet           quiet mode
    -u, --include-untracked
                          include untracked files in stash
    -a, --all             include ignore files
    -m, --message <message>
                          stash message
    --pathspec-from-file <file>
                          read pathspec from file
    --pathspec-file-nul   with --pathspec-from-file, pathspec elements are separated with NUL character


User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log --oneline
b201290 (HEAD -> ft/team-page, origin/ft/team-page) Add new team members
2ed7b74 (origin/ft/bundle-2, ft/bundle-2) Add Team Players
87b5aa9 Create Services.html File
8d97767 Merge pull request #1 from ishimweClaude12/dev
4d69ff9 Update README
6c8e42a Add Home, About and Team pages

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git stash b201290
fatal: subcommand wasn't specified; 'push' can't be assumed due
to unexpected token 'b201290'

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git stash list

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (main)
$ git stash list

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (main)
$ git brach
git: 'brach' is not a git command. See 'git --help'.

The most similar command is
        branch

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (main)
$ git branch
  ft/bundle-2
  ft/contact-page
  ft/service-redesign
  ft/team-page
* main

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'
Your branch is up to date with 'origin/ft/bundle-2'.

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git stash list

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git switch ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log
commit b2012903df6981db5e2569ca7d606b39b772ee8c (HEAD -> ft/team-page, origin/ft/team-page)
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Tue Jul 25 10:41:41 2023 +0200

    Add new team members

commit 2ed7b74f4a5f7e387a96c14cbb5715245fd12942 (origin/ft/bundle-2, ft/bundle-2)
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Fri Jul 14 09:25:41 2023 +0100

    Add Team Players

commit 87b5aa95bec6228dc5b650fb5b1c8b6e356d069e
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Thu Jul 13 10:30:44 2023 +0100

    Create Services.html File

commit 8d9776760d724d0085f09e2529b0641aa13e1ff4

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git cherry-pick b2012903df6981db5e2569ca7d606b39b772ee8~
[ft/contact-page b029dc6] Add Team Players
 Date: Fri Jul 14 09:25:41 2023 +0100
 1 file changed, 5 insertions(+)

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git sttus
git: 'sttus' is not a git command. See 'git --help'.

The most similar command is
        status

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git status
On branch ft/contact-page
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   team.html

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git add .

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git commit -m "Add Changes to the Team Page"
[ft/contact-page 8cb6ea9] Add Changes to the Team Page
 1 file changed, 2 insertions(+)

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git push --set-upstream origin ft/contact-page
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 757 bytes | 252.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/ishimweClaude12/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/ishimweClaude12/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git add .

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git commit -m "Add FAQ Page"
[ft/faq-page 75c0a71] Add FAQ Page
 1 file changed, 10 insertions(+)
 create mode 100644 faq.html

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 448 bytes | 224.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/ishimweClaude12/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/ishimweClaude12/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git log
commit 75c0a712bbb00a65b66745b216c77b82a0a53003 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Tue Jul 25 11:18:02 2023 +0200

    Add FAQ Page

commit 8cb6ea9b93671c743c8ecbed170aae3fd96829b9 (origin/ft/contact-page, ft/contact-page)
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Tue Jul 25 11:12:49 2023 +0200

    Add Changes to the Team Page

commit b029dc6a8093189d5c70a7a340d077acd53cfd9c
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Fri Jul 14 09:25:41 2023 +0100

    Add Team Players

commit 32f17e860efb08becd9b6f934d08093d4095cd7b (origin/main, or

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert 8cb6ea9b93671c743c8ecbed170aae3fd96829b91
fatal: bad revision '8cb6ea9b93671c743c8ecbed170aae3fd96829b91'

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git log
commit 75c0a712bbb00a65b66745b216c77b82a0a53003 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Tue Jul 25 11:18:02 2023 +0200

    Add FAQ Page

commit 8cb6ea9b93671c743c8ecbed170aae3fd96829b9 (origin/ft/contact-page, ft/contact-page)
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Tue Jul 25 11:12:49 2023 +0200

    Add Changes to the Team Page

commit b029dc6a8093189d5c70a7a340d077acd53cfd9c
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Fri Jul 14 09:25:41 2023 +0100

    Add Team Players

commit 32f17e860efb08becd9b6f934d08093d4095cd7b (origin/main, or

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert b029dc6a8093189d5c70a7a340d077acd53cfd9c1~
fatal: bad revision 'b029dc6a8093189d5c70a7a340d077acd53cfd9c1~'
User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert b029dc6a8093189d5c70a7a340d077acd53cfd9c1
fatal: bad revision 'b029dc6a8093189d5c70a7a340d077acd53cfd9c1'

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert b029dc6a8093189d5c70a7a340d077acd53cfd9c1
fatal: bad revision 'b029dc6a8093189d5c70a7a340d077acd53cfd9c1'

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git log
commit 75c0a712bbb00a65b66745b216c77b82a0a53003 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Tue Jul 25 11:18:02 2023 +0200

    Add FAQ Page

commit 8cb6ea9b93671c743c8ecbed170aae3fd96829b9 (origin/ft/contact-page, ft/contact-page)
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Tue Jul 25 11:12:49 2023 +0200

    Add Changes to the Team Page

commit b029dc6a8093189d5c70a7a340d077acd53cfd9c
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Fri Jul 14 09:25:41 2023 +0100

    Add Team Players

commit 32f17e860efb08becd9b6f934d08093d4095cd7b (origin/main, or

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert b029dc6a8093189d5c70a7a340d077acd53cfd9c
Auto-merging team.html
CONFLICT (content): Merge conflict in team.html
error: could not revert b029dc6... Add Team Players
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git status
On branch ft/faq-page
Your branch is up to date with 'origin/ft/faq-page'.

You are currently reverting commit b029dc6.
  (fix conflicts and run "git revert --continue")
  (use "git revert --skip" to skip this patch)
  (use "git revert --abort" to cancel the revert operation)

Unmerged paths:
  (use "git restore --staged <file>..." to unstage)
  (use "git add <file>..." to mark resolution)
        both modified:   team.html

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git revert --continue
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
U       team.html

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git revert --continue
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
U       team.html

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git revert --continue
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
U       team.html

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git revert --continue
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
U       team.html

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git status
You are currently reverting commit b029dc6.
  (all conflicts fixed: run "git revert --continue")
  (use "git revert --skip" to skip this patch)
  (use "git revert --abort" to cancel the revert operation)

nothing to commit, working tree clean

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git push
Everything up-to-date                                           olutions (ft/faq-page|REVERTING)

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git checkout main                                             olutions (ft/faq-page|REVERTING)
Switched to branch 'main'
warning: cancelling a revert in progress
Your branch is up to date with 'origin/main'.

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (main)                                                 olutions (main)
$ git branch ft/home-page-redesign

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (main)
$ git branch
  ft/bundle-2
  ft/contact-page
  ft/faq-page
  ft/home-page-redesign
  ft/service-redesign
  ft/team-page
* main

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (main)
$ git commit -a -m "Add NavBar to the home page"
[main b0a4d7f] Add NavBar to the home page
 1 file changed, 7 insertions(+)

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 373 bytes | 373.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ishimweClaude12/Gym-Git-Exercise-Solutions.git
   32f17e8..b0a4d7f  main -> main

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git status
On branch ft/home-page-redesign
nothing to commit, working tree clean

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git log
commit 32f17e860efb08becd9b6f934d08093d4095cd7b (HEAD -> ft/home-page-redesign)
Merge: 8d97767 2c7f8b4
Author: Claude <77576560+ishimweClaude12@users.noreply.github.com>
Date:   Thu Jul 13 11:07:23 2023 +0100

    Merge pull request #3 from ishimweClaude12/ft/service-redesign

    Git: Bundle-2 Exercise-2

commit 2c7f8b40d3801ec2b28950f750146c5526f90f3b (origin/ft/service-redesign, ft/service-redesign)
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Thu Jul 13 11:00:31 2023 +0100

    Add Changes to services.html File

commit 87b5aa95bec6228dc5b650fb5b1c8b6e356d069e
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git log --oneline
32f17e8 (HEAD -> ft/home-page-redesign) Merge pull request #3 from ishimweClaude12/ft/service-redesign
2c7f8b4 (origin/ft/service-redesign, ft/service-redesign) Add Changes to services.html File
87b5aa9 Create Services.html File
8d97767 Merge pull request #1 from ishimweClaude12/dev
4d69ff9 Update README
6c8e42a Add Home, About and Team pages
34e239d Change some html elements and styles.css
2e21de9 Add README File
3dba784 Add styles.css and heading title to the html file

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git log
commit b0a4d7f12055bd23beaa7f11cbc083caea230830 (HEAD -> ft/home-page-redesign, origin/main, origin/HEAD, main)
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>
Date:   Tue Jul 25 13:25:08 2023 +0200

    Add NavBar to the home page

commit 32f17e860efb08becd9b6f934d08093d4095cd7b
Merge: 8d97767 2c7f8b4
Author: Claude <77576560+ishimweClaude12@users.noreply.github.com>
Date:   Thu Jul 13 11:07:23 2023 +0100

    Merge pull request #3 from ishimweClaude12/ft/service-redesign

    Git: Bundle-2 Exercise-2

commit 2c7f8b40d3801ec2b28950f750146c5526f90f3b (origin/ft/service-redesign, ft/service-redesign)
Author: Claude Ishimwe <dpqb12haikuo@gmail.com>

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git commit -a -m 'Add Sign Up link'
[ft/home-page-redesign d07f9a9] Add Sign Up link
 1 file changed, 1 insertion(+)

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git push
fatal: The current branch ft/home-page-redesign has no upstream
branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 317 bytes | 317.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/ishimweClaude12/Gym-Git-Exercise-Solutions/pull/new/ft/home-page-redesign
remote:
To https://github.com/ishimweClaude12/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (main)
$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 644 bytes | 214.00 KiB/s, done.
From https://github.com/ishimweClaude12/Gym-Git-Exercise-Solutions
   b0a4d7f..0143e24  main       -> origin/main
Updating b0a4d7f..0143e24
Fast-forward
 home.html | 1 +
 1 file changed, 1 insertion(+)

User@DESKTOP-3M65OUK MINGW64 ~/Desktop/TheGym/Gym-Git-Exercise-Solutions (main)
$
```
