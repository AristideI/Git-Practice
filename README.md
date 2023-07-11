
walte@Walter MINGW64 ~
$ cd d:

walte@Walter MINGW64 /d
$ ls
'$RECYCLE.BIN'/                alu-higher_level_programming/
'1. Front-End'/                alu-web-development/
 Fix_My_Code_Challenge/        binary_trees/
 Git-Practice/                 ojemba-x-gym-assignment-group-1-AristideI/
 HTML-CSS_Contest/             pro/
 JavaScript30/                 prooo/
 Library-App/                  saturday-clone/
'System Volume Information'/   tailwind-landing-page/
'The Gym'/                     untitled0.py
 Wes-Bos-Video-Notes/

walte@Walter MINGW64 /d
$ cd Git-Practice/

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ vi home.html

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stach push -m "one"
git: 'stach' is not a git command. See 'git --help'.

The most similar command is
        stash

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stash push -m "one"
No local changes to save

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stash push -m "one"
No local changes to save

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stash list

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stash
No local changes to save

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ ls
file1.html  file2  file3  file5  file6  home.html

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ touch filee2

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git add .
warning: in the working copy of 'home.html', LF will be replaced by CRLF the next time Git touches it

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git commit -m "The saint"
[dev2 7d1a730] The saint
 2 files changed, 2 insertions(+)
 create mode 100644 filee2
 create mode 100644 home.html

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ vi home.html

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stash push -m "one"
warning: in the working copy of 'home.html', LF will be replaced by CRLF the next time Git touches it
Saved working directory and index state On dev2: one

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ vi about.html

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stash push -m "two"
No local changes to save

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ touch about.html team.html

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git add .
warning: in the working copy of 'about.html', LF will be replaced by CRLF the next time Git touches it

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git commit -m "Stash"
[dev2 95156f8] Stash
 2 files changed, 3 insertions(+)
 create mode 100644 about.html
 create mode 100644 team.html

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stash list
stash@{0}: On dev2: one

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ vi about.html

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stash push -m "two"
warning: in the working copy of 'about.html', LF will be replaced by CRLF the next time Git touches it
Saved working directory and index state On dev2: two

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ vi team.html

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stash push -m "three"
warning: in the working copy of 'team.html', LF will be replaced by CRLF the next time Git touches it
Saved working directory and index state On dev2: three

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stash list
stash@{0}: On dev2: three
stash@{1}: On dev2: two
stash@{2}: On dev2: one

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stash apply 2
On branch dev2
Your branch is ahead of 'Git-Practice/dev2' by 2 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stash pop 1
On branch dev2
Your branch is ahead of 'Git-Practice/dev2' by 2 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   about.html
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{1} (7780e755d822f649aec3766c5fbe14095d891297)

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git stash pop 1
error: Your local changes to the following files would be overwritten by merge:
        home.html
Please commit your changes or stash them before you merge.
Aborting
On branch dev2
Your branch is ahead of 'Git-Practice/dev2' by 2 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   about.html
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")
The stash entry is kept in case you need it again.

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git add .

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ git commit -m "finished with stash"
[dev2 6fa2818] finished with stash
 2 files changed, 5 insertions(+), 1 deletion(-)

walte@Walter MINGW64 /d/Git-Practice (dev2)
$ ^C

walt
