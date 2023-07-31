# Git Exercises Solutions

## Bundle 3

### Exercise 2

```bash

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'
Your branch is up to date with 'origin/ft/faq-page'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$ git branch -b ft/home-page-redesign
error: unknown switch `b'
usage: git branch [<options>] [-r | -a] [--merged] [--no-merged]
   or: git branch [<options>] [-f] [--recurse-submodules] <branch-name> [<start-point>]
   or: git branch [<options>] [-l] [<pattern>...]
   or: git branch [<options>] [-r] (-d | -D) <branch-name>...
   or: git branch [<options>] (-m | -M) [<old-branch>] <new-branch>
   or: git branch [<options>] (-c | -C) [<old-branch>] <new-branch>
   or: git branch [<options>] [-r | -a] [--points-at]
   or: git branch [<options>] [-r | -a] [--format]

Generic options
    -v, --verbose         show hash and subject, give twice for upstream branch
    -q, --quiet           suppress informational messages
    -t, --track[=(direct|inherit)]
                          set branch tracking configuration
    -u, --set-upstream-to <upstream>
                          change the upstream info
    --unset-upstream      unset the upstream info
    --color[=<when>]      use colored output
    -r, --remotes         act on remote-tracking branches
    --contains <commit>   print only branches that contain the commit
    --no-contains <commit>
                          print only branches that don't contain the commit
    --abbrev[=<n>]        use <n> digits to display object names

Specific git-branch actions:
    -a, --all             list both remote-tracking and local branches
    -d, --delete          delete fully merged branch
    -D                    delete branch (even if not merged)
    -m, --move            move/rename a branch and its reflog
    -M                    move/rename a branch, even if target exists
    --omit-empty          do not output a newline after empty formatted refs
    -c, --copy            copy a branch and its reflog
    -C                    copy a branch, even if target exists
    -l, --list            list branch names
    --show-current        show current branch name
    --create-reflog       create the branch's reflog
    --edit-description    edit the description for the branch
    -f, --force           force creation, move/rename, deletion
    --merged <commit>     print only branches that are merged
    --no-merged <commit>  print only branches that are not merged
    --column[=<style>]    list branches in columns
    --sort <key>          field name to sort on
    --points-at <object>  print only branches of the object
    -i, --ignore-case     sorting and filtering are case insensitive
    --recurse-submodules  recurse through submodules
    --format <format>     format to use for the output


User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$ git branch ft/home-page-redesign

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$ git switch ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git add index.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git commit -m
error: switch `m' requires a value


User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git commit -m "updated the index.html page"
[main b68d8ad] updated the index.html page
 1 file changed, 1 insertion(+), 1 deletion(-)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 303 bytes | 303.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/HIRWA13/Git-Exercises.git
   6050b44..b68d8ad  main -> main

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git switch ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/home-page-redesign)
$ git status
On branch ft/home-page-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/home-page-redesign)
$ git add home.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/home-page-redesign)
$ git commit -m "added changes on the homepage"
[ft/home-page-redesign 36f7dea] added changes on the homepage
 1 file changed, 2 insertions(+), 5 deletions(-)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/home-page-redesign)
$ git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 12 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (8/8), 936 bytes | 936.00 KiB/s, done.
Total 8 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting
remote:      https://github.com/HIRWA13/Git-Exercises/pull/new/ft/home-page-redesign
remote:
To https://github.com/HIRWA13/Git-Exercises.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/home-page-redesign)
$


```