
walte@Walter MINGW64 /d
$ mkdir Git-Practice

walte@Walter MINGW64 /d
$ cd Git-Practice/

walte@Walter MINGW64 /d/Git-Practice
$ git init
Initialized empty Git repository in D:/Git-Practice/.git/

walte@Walter MINGW64 /d/Git-Practice (master)
$ git branch -m master main

walte@Walter MINGW64 /d/Git-Practice (main)
$ vi file1.html

walte@Walter MINGW64 /d/Git-Practice (main)
$ touch file2 file3

walte@Walter MINGW64 /d/Git-Practice (main)
$ git add .
warning: in the working copy of 'file1.html', LF will be replaced by CRLF the next time Git touches it

walte@Walter MINGW64 /d/Git-Practice (main)
$ git commit -m "Initialising git"
[main (root-commit) 7c6ccad] Initialising git
 3 files changed, 1 insertion(+)
 create mode 100644 file1.html
 create mode 100644 file2
 create mode 100644 file3

walte@Walter MINGW64 /d/Git-Practice (main)
$ git remote add https://github.com/AristideI/Git-Practice.git
usage: git remote add [<options>] <name> <url>

    -f, --fetch           fetch the remote branches
    --tags                import all tags and associated objects when fetching
                          or do not fetch any tag at all (--no-tags)
    -t, --track <branch>  branch(es) to track
    -m, --master <branch>
                          master branch
    --mirror[=(push|fetch)]
                          set up remote as a mirror to push to or fetch from


walte@Walter MINGW64 /d/Git-Practice (main)
$ git remote add Git-Practice https://github.com/AristideI/Git-Practice.git

walte@Walter MINGW64 /d/Git-Practice (main)
$ git commit -m "initialising git repo"
On branch main
nothing to commit, working tree clean

walte@Walter MINGW64 /d/Git-Practice (main)
$ git add .

walte@Walter MINGW64 /d/Git-Practice (main)
$ git commit -m "initialising git repo"
On branch main
nothing to commit, working tree clean

walte@Walter MINGW64 /d/Git-Practice (main)
$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream Git-Practice main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


walte@Walter MINGW64 /d/Git-Practice (main)
$ git push --set-upstream Git-practice main
fatal: 'Git-practice' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

walte@Walter MINGW64 /d/Git-Practice (main)
$ git push --set-upstream main
fatal: 'main' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

walte@Walter MINGW64 /d/Git-Practice (main)
$ git push --set-upstream Git-practice main
fatal: 'Git-practice' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

walte@Walter MINGW64 /d/Git-Practice (main)
$ git push --set-upstream Git-Practice main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 274 bytes | 274.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/AristideI/Git-Practice.git
 * [new branch]      main -> main
branch 'main' set up to track 'Git-Practice/main'.

walte@Walter MINGW64 /d/Git-Practice (main)
$ git branch -b dev
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


walte@Walter MINGW64 /d/Git-Practice (main)
$ git checkout -b dev
Switched to a new branch 'dev'

walte@Walter MINGW64 /d/Git-Practice (dev)
$ git checkout -b test
Switched to a new branch 'test'

walte@Walter MINGW64 /d/Git-Practice (test)
$ git checkout dev
Switched to branch 'dev'

walte@Walter MINGW64 /d/Git-Practice (dev)
$ git branch -D test
Deleted branch test (was 7c6ccad).

walte@Walter MINGW64 /d/Git-Practice (dev)
$ git push origin dev
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

walte@Walter MINGW64 /d/Git-Practice (dev)
$ git push dev
fatal: 'dev' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

walte@Walter MINGW64 /d/Git-Practice (dev)
$ git push origin dev
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

walte@Walter MINGW64 /d/Git-Practice (dev)
$ git add .

walte@Walter MINGW64 /d/Git-Practice (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream Git-Practice dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


walte@Walter MINGW64 /d/Git-Practice (dev)
$ git commit -m "Adding to dev"
On branch dev
nothing to commit, working tree clean

walte@Walter MINGW64 /d/Git-Practice (dev)
$ git push --set-upstream Git-Practice main
Everything up-to-date
branch 'main' set up to track 'Git-Practice/main'.

walte@Walter MINGW64 /d/Git-Practice (dev)
$ touch file5

walte@Walter MINGW64 /d/Git-Practice (dev)
$ git add .

walte@Walter MINGW64 /d/Git-Practice (dev)
$ git commit -m "modify=ing file5"
[dev e2bb3e8] modify=ing file5
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 file5

walte@Walter MINGW64 /d/Git-Practice (dev)
$ git push origin dev
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

walte@Walter MINGW64 /d/Git-Practice (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream Git-Practice dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


walte@Walter MINGW64 /d/Git-Practice (dev)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'Git-Practice/main'.

walte@Walter MINGW64 /d/Git-Practice (main)
$ vi README.md

walte@Walter MINGW64 /d/Git-Practice (main)
$

