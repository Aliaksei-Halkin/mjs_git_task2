Hello world! first test vim
Hello GIT! second test, create changes
 Paste my changes from git console:

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git
$ git init
Initialized empty Git repository in D:/JavaLab/mod1_git/.git/

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ ls -l
total 0

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ ^C

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ touch README.md

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ vim README.md

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git add .
warning: LF will be replaced by CRLF in README.md.
The file will have its original line endings in your working directory

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md


Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git commit -m "created readme"
[master (root-commit) a0efd7a] created readme
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git status
On branch master
nothing to commit, working tree clean

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git checkout -b develop
Switched to a new branch 'develop'

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (develop)
$ git  checkout -b git_task

Switched to a new branch 'git_task'

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_task)
$

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_task)
$ git checkout -b git_0
Switched to a new branch 'git_0'

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_0)
$ git show-branch
! [develop] created readme
 * [git_0] created readme
  ! [git_task] created readme
   ! [master] created readme
----
+*++ [develop] created readme

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_0)
$ vim README.md

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_0)
$ git status
On branch git_0
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_0)
$ git add.
git: 'add.' is not a git command. See 'git --help'.

The most similar command is
        add

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_0)
$ git add .
warning: LF will be replaced by CRLF in README.md.
The file will have its original line endings in your working directory

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_0)
$ git status
On branch git_0
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md


Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_0)
$ git diff --cached
diff --git a/README.md b/README.md
index 79a5284..37ac54b 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,2 @@
 Hello world! first test vim
+Hello GIT! second test, create changes

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_0)
$ git commit -m "added git_0 line to readme file"
[git_0 a0ba936] added git_0 line to readme file
 1 file changed, 1 insertion(+)

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_0)
$ git status
On branch git_0
nothing to commit, working tree clean

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_0)
$ git checkout git_task
Switched to branch 'git_task'

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_task)
$ git merge git_0 --no-ff^C

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_task)
$ git merge git_0 --no-ff
Merge made by the 'recursive' strategy.
 README.md | 1 +
 1 file changed, 1 insertion(+)

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_task)
$ gitk
g
Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_task)
$ git show-branch
! [develop] created readme
 ! [git_0] added git_0 line to readme file
  * [git_task] Merge branch 'git_0' into git_task
   ! [master] created readme
----
  -  [git_task] Merge branch 'git_0' into git_task
 +*  [git_0] added git_0 line to readme file
++*+ [develop] created readme

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (git_task)
$ git checkout develop
Switched to branch 'develop'

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (develop)
$ git merge git_task --no--ff
error: unknown option `no--ff'
usage: git merge [<options>] [<commit>...]
   or: git merge --abort
   or: git merge --continue

    -n                    do not show a diffstat at the end of the merge
    --stat                show a diffstat at the end of the merge
    --summary             (synonym to --stat)
    --log[=<n>]           add (at most <n>) entries from shortlog to merge commit message
    --squash              create a single commit instead of doing a merge
    --commit              perform a commit if the merge succeeds (default)
    -e, --edit            edit message before committing
    --cleanup <mode>      how to strip spaces and #comments from message
    --ff                  allow fast-forward (default)
    --ff-only             abort if fast-forward is not possible
    --rerere-autoupdate   update the index with reused conflict resolution if possible
    --verify-signatures   verify that the named commit has a valid GPG signature
    -s, --strategy <strategy>
                          merge strategy to use
    -X, --strategy-option <option=value>
                          option for selected merge strategy
    -m, --message <message>
                          merge commit message (for a non-fast-forward merge)
    -F, --file <path>     read message from file
    -v, --verbose         be more verbose
    -q, --quiet           be more quiet
    --abort               abort the current in-progress merge
    --quit                --abort but leave index and working tree alone
    --continue            continue the current in-progress merge
    --allow-unrelated-histories
                          allow merging unrelated histories
    --progress            force progress reporting
    -S, --gpg-sign[=<key-id>]
                          GPG sign commit
    --overwrite-ignore    update ignored files (default)
    --signoff             add Signed-off-by:
    --no-verify           bypass pre-merge-commit and commit-msg hooks


Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (develop)
$ ^C

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (develop)
$ git merge git_task --no-ff
Merge made by the 'recursive' strategy.
 README.md | 1 +
 1 file changed, 1 insertion(+)

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (develop)
$ git checkout master
Switched to branch 'master'

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git merge develop --no--ff
error: unknown option `no--ff'
usage: git merge [<options>] [<commit>...]
   or: git merge --abort
   or: git merge --continue

    -n                    do not show a diffstat at the end of the merge
    --stat                show a diffstat at the end of the merge
    --summary             (synonym to --stat)
    --log[=<n>]           add (at most <n>) entries from shortlog to merge commit message
    --squash              create a single commit instead of doing a merge
    --commit              perform a commit if the merge succeeds (default)
    -e, --edit            edit message before committing
    --cleanup <mode>      how to strip spaces and #comments from message
    --ff                  allow fast-forward (default)
    --ff-only             abort if fast-forward is not possible
    --rerere-autoupdate   update the index with reused conflict resolution if possible
    --verify-signatures   verify that the named commit has a valid GPG signature
    -s, --strategy <strategy>
                          merge strategy to use
    -X, --strategy-option <option=value>
                          option for selected merge strategy
    -m, --message <message>
                          merge commit message (for a non-fast-forward merge)
    -F, --file <path>     read message from file
    -v, --verbose         be more verbose
    -q, --quiet           be more quiet
    --abort               abort the current in-progress merge
    --quit                --abort but leave index and working tree alone
    --continue            continue the current in-progress merge
    --allow-unrelated-histories
                          allow merging unrelated histories
    --progress            force progress reporting
    -S, --gpg-sign[=<key-id>]
                          GPG sign commit
    --overwrite-ignore    update ignored files (default)
    --signoff             add Signed-off-by:
    --no-verify           bypass pre-merge-commit and commit-msg hooks


Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git merge develop --no-f
hint: Waiting for your editor to close the file...       1 [sig] bash 977! sigpacket::process: Suppressing signal 18 to win32 process (pid 8836)
 248003 [sig] bash 977! sigpacket::process: Suppressing signal 18 to win32 process (pid 8836)
1880172 [sig] bash 977! sigpacket::process: Suppressing signal 18 to win32 process (pid 8836)
2551270 [sig] bash 977! sigpacket::process: Suppressing signal 18 to win32 process (pid 8836)
Merge made by the 'recursive' strategy.
 README.md | 1 +
 1 file changed, 1 insertion(+)

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git log --all --graph --decorate --oneline --simplify-by-decoration
* 1b83c6d (HEAD -> master) Merge branch 'develop'
* a4b362c (develop) Merge branch 'git_task' into develop
* 31decb1 (git_task) Merge branch 'git_0' into git_task
* a0ba936 (git_0) added git_0 line to readme file
* a0efd7a created readme

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git log --graph --oneline –all command
fatal: ambiguous argument '–all': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git log --graph --oneline --all command
fatal: ambiguous argument 'command': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git log --graph --oneline –-all
fatal: ambiguous argument '–-all': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$ git log --graph --oneline –all
fatal: ambiguous argument '–all': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

Alex@DESKTOP-JH9NJGL MINGW64 /d/JavaLab/mod1_git (master)
$

