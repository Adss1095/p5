# p5
Exp_5


git@ise:~$ cd 1mv23ai002
git@ise:~/1mv23ai002$ mkdir exp5
git@ise:~/1mv23ai002$ cd exp005
git@ise:~/1mv23ai002/exp005$ echo "# program5" >> README.md
git@ise:~/1mv23ai002/exp005$ git init
Initialized empty Git repository in /home/git/1mv23ai002/exp005/.git/
git@ise:~/1mv23ai002/exp005$ git add README.md
git@ise:~/1mv23ai002/exp005$ git commit -m "first commit"
[master (root-commit) 660fcb0] first commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
git@ise:~/1mv23ai002/exp005$ git branch -M main
git@ise:~/1mv23ai002/exp005$ git remote add origin https://github.com/ads1095/program5.git
git@ise:~/1mv23ai002/exp005$ git push -u origin main
Username for 'https://github.com': ads1095
Password for 'https://ads1095@github.com':
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 221 bytes | 221.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/ads1095/program5.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
git@ise:~/1mv23ai002/exp005$
it@ise:~/1mv23ai002/exp005$ ls
README.md
git@ise:~/1mv23ai002/exp005$ gedit README.md
git@ise:~/1mv23ai002/exp005$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
git@ise:~/1mv23ai002/exp005$ git add README.md
git@ise:~/1mv23ai002/exp005$ git commit -m "made changes"
[main 53ddd02] made changes
 1 file changed, 1 insertion(+)
git@ise:~/1mv23ai002/exp005$ git fetch
Username for 'https://github.com': ads1095
Password for 'https://ads1095@github.com':
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 906 bytes | 906.00 KiB/s, done.
From https://github.com/ads1095/program5
   5e5d49f..dc587a2  main       -> origin/main
git@ise:~/1mv23ai002/exp005$ git rebase origin/main
First, rewinding head to replay your work on top of it...
Applying: made changes
Using index info to reconstruct a base tree...
M README.md
Falling back to patching base and 3-way merge...
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
error: Failed to merge in the changes.
Patch failed at 0001 made changes
hint: Use 'git am --show-current-patch' to see the failed patch
Resolve all conflicts manually, mark them as resolved with
"git add/rm <conflicted_files>", then run "git rebase --continue".
You can instead skip this commit: run "git rebase --skip".
To abort and get back to the state before "git rebase", run "git rebase --abort".
git@ise:~/1mv23ai002/exp005$ gedit README.md
git@ise:~/1mv23ai002/exp005$ git status
rebase in progress; onto dc587a2
You are currently rebasing branch 'main' on 'dc587a2'.
  (fix conflicts and then run "git rebase --continue")
  (use "git rebase --skip" to skip this patch)
  (use "git rebase --abort" to check out the original branch)

Unmerged paths:
  (use "git restore --staged <file>..." to unstage)
  (use "git add <file>..." to mark resolution)
both modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
git@ise:~/1mv23ai002/exp005$ git add .
git@ise:~/1mv23ai002/exp005$ git status
rebase in progress; onto dc587a2
You are currently rebasing branch 'main' on 'dc587a2'.
  (all conflicts fixed: run "git rebase --continue")

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
modified:   README.md

git@ise:~/1mv23ai002/exp005$ git rebase --continue
Applying: made changes
git@ise:~/1mv23ai002/exp005$ git push -u origin main
Username for 'https://github.com': ads1095
Password for 'https://ads1095@github.com':
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/ads1095/program5.git/'
git@ise:~/1mv23ai002/exp005$ git push -u origin main
Username for 'https://github.com': ads1095
Password for 'https://\ads1095@github.com':
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 297 bytes | 297.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/ads1095/program5.git
   dc587a2..fad64df  main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
