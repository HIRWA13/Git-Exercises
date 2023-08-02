# Git Exercises:

## Bundle 4 Exercise 2:

```bash

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git checkout ft/footer
Switched to branch 'ft/footer'
Your branch is up to date with 'origin/ft/footer'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/footer)
$ git status
On branch ft/footer
Your branch is up to date with 'origin/ft/footer'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   footer.html

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/footer)
$ git add footer.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/footer)
$ git commit -m "updated the footer.html page"
[ft/footer 931abc0] updated the footer.html page
 1 file changed, 5 insertions(+)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/footer)
$ git status
On branch ft/footer
Your branch is ahead of 'origin/ft/footer' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/footer)
$ git add home.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/footer)
$ git commit -m "updated the home.html"
[ft/footer 7ed7d9e] updated the home.html
 1 file changed, 5 deletions(-)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/footer)
$ git push origin
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 669 bytes | 334.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), completed with 3 local objects.
To https://github.com/HIRWA13/Git-Exercises.git
   84874f1..7ed7d9e  ft/footer -> ft/footer

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/footer)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'git-copy/main' by 1 commit.
  (use "git push" to publish your local commits)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$  git log --online
fatal: unrecognized argument: --online

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git log --oneline
238a8a6 (HEAD -> main) updated the footer component
6cb5b94 (origin/main, git-copy/main) updated the README file
1250274 updated the README file on main
7edd260 updated the README file
0a32b8f updated the contents of the home.html and added the nav container
f2cc936 updated the README.md
7b4bd41 added a README file
b68d8ad updated the index.html page
6050b44 Merge branch 'main' of https://github.com/HIRWA13/Git-Exercises
db6435d changed the index.html page
466157f Merge pull request #4 from HIRWA13/ft/contact-page
a04e25a (origin/ft/contact-page, ft/contact-page) added the contact us page
f8d755b added the team page
4997146 Merge pull request #3 from HIRWA13/ft/team-page
ee801c8 (origin/ft/team-page, ft/team-page) added the team page
eff90ca resolved the conflicts
pick 6cb5b94 updated the README file


Successfully rebased and updated refs/heads/main.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git log --oneline
c623a0d (HEAD -> main) fix changes
238a8a6 updated the footer component
6cb5b94 (origin/main, git-copy/main) updated the README file
1250274 updated the README file on main
7edd260 updated the README file
0a32b8f updated the contents of the home.html and added the nav container
f2cc936 updated the README.md
#                    commit's log message, unless -C is used, in which case

Successfully rebased and updated refs/heads/ft/squashing.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/squashing)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'git-copy/main' by 2 commits.
  (use "git push" to publish your local commits)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git merge ft/footer
Auto-merging footer.html
CONFLICT (add/add): Merge conflict in footer.html
Auto-merging home.html
CONFLICT (content): Merge conflict in home.html
Automatic merge failed; fix conflicts and then commit the result.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main|MERGING)
$ git status
On branch main
Your branch is ahead of 'git-copy/main' by 2 commits.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both added:      footer.html
        both modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main|MERGING)
$ git add --all

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main|MERGING)
$ git status
On branch main
Your branch is ahead of 'git-copy/main' by 2 commits.
  (use "git push" to publish your local commits)

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   footer.html
        modified:   home.html


User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main|MERGING)
$ git commit -m "changed the footer component and the home page"
[main 265f895] changed the footer component and the home page

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git checkout ft/squashing
Switched to branch 'ft/squashing'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/squashing)
$ git log --oneline
c623a0d (HEAD -> ft/squashing) fix changes
238a8a6 updated the footer component
6cb5b94 (origin/main, git-copy/main) updated the README file
1250274 updated the README file on main
7edd260 updated the README file
0a32b8f updated the contents of the home.html and added the nav container
f2cc936 updated the README.md
7b4bd41 added a README file
b68d8ad updated the index.html page
6050b44 Merge branch 'main' of https://github.com/HIRWA13/Git-Exercises
db6435d changed the index.html page
466157f Merge pull request #4 from HIRWA13/ft/contact-page
a04e25a (origin/ft/contact-page, ft/contact-page) added the contact us page
f8d755b added the team page
4997146 Merge pull request #3 from HIRWA13/ft/team-page
ee801c8 (origin/ft/team-page, ft/team-page) added the team page
eff90ca resolved the conflicts
88b2400 Merge branch 'main' of https://github.com/HIRWA13/Git-Exercises
35dd828 changes to the services.html
8bad055 (origin/ft/service-redesign, ft/service-redesign) modified the services.html page
bd7250b Merge pull request #1 from HIRWA13/ft/bundle-2
3f35f55 (origin/ft/bundle-2, ft/bundle-2) added the services.html page

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/squashing)
$ git merge --squash ft/footer
Auto-merging footer.html
CONFLICT (add/add): Merge conflict in footer.html
Auto-merging home.html
CONFLICT (content): Merge conflict in home.html
Squash commit -- not updating HEAD
Automatic merge failed; fix conflicts and then commit the result.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/squashing)
$ git add --all

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/squashing)
$ git commit -m "updated the footer and the homepage"
[ft/squashing 7e87691] updated the footer and the homepage
 2 files changed, 6 insertions(+), 3 deletions(-)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/squashing)
$ git merge --squash ft/footer
Auto-merging home.html
Automatic merge went well; stopped before committing as requested
Squash commit -- not updating HEAD

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/squashing)
$ git merge --squash ft/footer
Auto-merging home.html
Automatic merge went well; stopped before committing as requested
Squash commit -- not updating HEAD

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/squashing)
$ git status
On branch ft/squashing
nothing to commit, working tree clean

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/squashing)
$ git push -u origin ft/squashing
Enumerating objects: 12, done.
Counting objects: 100% (12/12), done.
Delta compression using up to 12 threads
Compressing objects: 100% (10/10), done.
Writing objects: 100% (10/10), 1.16 KiB | 1.16 MiB/s, done.
Total 10 (delta 6), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (6/6), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/HIRWA13/Git-Exercises/pull/new/ft/squashing
remote:
To https://github.com/HIRWA13/Git-Exercises.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/squashing)
$ touch README.md

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/squashing)
$ ls
README.md   contact.html  home.html   services.html  team.html
about.html  footer.html   index.html  style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/squashing)
$

```