# AdvancedGit
Missing File Fix 
```
HP-@isaacb24 MINGW64 /d/web
$ cd 'd:/web/AdvancedGit'

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git add test1.md && git commit -m "chore: Create initial file"
fatal: pathspec 'test1.md' did not match any files

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git add test1.md && git commit -m "chore: Create initial file"
fatal: pathspec 'test1.md' did not match any files

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ ls test1.md
ls: cannot access 'test1.md': No such file or directory

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ touch test1.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ touch test2.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ touch test3.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ touch test4.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git add test1.md && git commit -m "chore: Create initial file"
[main (root-commit) 2e6f90b] chore: Create initial file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git add test2.md && git commit -m "chore: Create another file"
[main 8e40dfd] chore: Create another file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git add test3.md && git commit -m "chore: Create third and fourth files"
[main f6bfa1f] chore: Create third and fourth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git status
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test4.md

nothing added to commit but untracked files present (use "git add" to track)

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git log
commit f6bfa1fa72135a13f25afe24ca3181b50e4446d1 (HEAD -> main)
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:27:17 2025 +0200

    chore: Create third and fourth files

commit 8e40dfd889209cdf16958bb98ee60a9beab31e62
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:27:09 2025 +0200

    chore: Create another file

commit 2e6f90bd2b095e27d3fb6a4a2d331d5ed841a55f
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:26:59 2025 +0200

:
commit f6bfa1fa72135a13f25afe24ca3181b50e4446d1 (HEAD -> main)
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:27:17 2025 +0200

    chore: Create third and fourth files

commit 8e40dfd889209cdf16958bb98ee60a9beab31e62
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:27:09 2025 +0200

    chore: Create another file

commit 2e6f90bd2b095e27d3fb6a4a2d331d5ed841a55f
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:26:59 2025 +0200

:
commit f6bfa1fa72135a13f25afe24ca3181b50e4446d1 (HEAD -> main)
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:27:17 2025 +0200

    chore: Create third and fourth files

commit 8e40dfd889209cdf16958bb98ee60a9beab31e62
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:27:09 2025 +0200

    chore: Create another file

commit 2e6f90bd2b095e27d3fb6a4a2d331d5ed841a55f
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:26:59 2025 +0200


HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git add test4.md && git commit -m "chore: Create fourth files"
[main f2b86b6] chore: Create fourth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test4.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
```

Editing Commit History:

```
HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git rebase -i HEAD~2
Successfully rebased and updated refs/heads/main.


HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git rebase -i HEAD~3
Stopped at 8e40dfd...  chore: Create another file
You can amend the commit now, with

  git commit --amend

Once you are satisfied with your changes, run

  git rebase --continue

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main|REBASE 1/3)
$ git commit --amend -m"Create second file"
[detached HEAD 90ed136] Create second file
 Date: Mon Jul 21 14:27:09 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main|REBASE 1/3)
$ git rebase --continue
Successfully rebased and updated refs/heads/main.

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
```
Keeping History Tidy - Squashing Commits:

```
HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ touch test{4..6}.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git add test5.md && git commit -m "chore: Create fifth files"
[main fa09252] chore: Create fifth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test5.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git add test6.md && git commit -m "chore: Create sixth files"
[main 5af2c4c] chore: Create sixth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test6.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git rebase -i Head~6
fatal: invalid upstream 'Head~6'

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git rebase -i Head~5
hint: Waiting for your editor to close the file... 
[detached HEAD 7671dd1] chore: Create fifth files
 Date: Mon Jul 28 11:16:27 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test5.md
 create mode 100644 test6.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main|REBASE 5/5)
```
Splitting a Commit:

```
HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git rebase -i Head~4
error: cannot rebase: You have unstaged changes.
error: Please commit or stash them.

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git commit --amend -m'chore:create third and fourth files'
[main b4c81c5] chore:create third and fourth files
 Date: Mon Jul 28 11:16:27 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test5.md
 create mode 100644 test6.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git add test4.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git commit --amend -m'chore:create third and fourth files'
[main 12588ee] chore:create third and fourth files
 Date: Mon Jul 28 11:16:27 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test5.md
 create mode 100644 test6.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git rebase -i Head~4
Stopped at 12588ee...  chore:create third and fourth files
You can amend the commit now, with

  git commit --amend

Once you are satisfied with your changes, run

  git rebase --continue

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main|REBASE 4/4)
$ git reset Head~1

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main|REBASE 4/4)
$ git reset Head~2

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main|REBASE 4/4)
$ git add test3.md 

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main|REBASE 4/4)
$ git commit -m 'create third file'
[detached HEAD c60b632] create third file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main|REBASE 4/4)
$ git add test4.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main|REBASE 4/4)
$ git commit -m 'create fourth file'
[detached HEAD 0bc8e11] create fourth file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test4.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main|REBASE 4/4)
$ git rebase --continue
Successfully rebased and updated refs/heads/main.

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
```
Advanced Squashing:
```
HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git rebase -i Head~4
fatal: invalid upstream 'Head~4'

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git rebase -i Head~3
hint: Waiting for your editor to close the file... 
[detached HEAD 59d31cd] create third file
 Date: Mon Jul 28 11:46:40 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main|REBASE 3/3)
$ qq
bash: qq: command not found

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main|REBASE 3/3)
$ git rebase --continue
Successfully rebased and updated refs/heads/main.

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
```
Dropping a Commit:

```
HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git add unwanted.txt 

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git commit -m 'commited unwated.txt'
[main 60c950b] commited unwated.txt
 1 file changed, 1 insertion(+)
 create mode 100644 unwanted.txt

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git push
To https://github.com/isaacbenit/AdvancedGit.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/isaacbenit/AdvancedGit.git'        
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git rebase -i Head~3
Successfully rebased and updated refs/heads/main.

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
```
Reordering Commits:
```
HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git rebase -i Head~3
Successfully rebased and updated refs/heads/main.

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ ^C

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git rebase -i Head~3
fatal: invalid upstream 'Head~3'

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git rebase -i Head~2
Successfully rebased and updated refs/heads/main.

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
```
cherry-pick commits:
```
HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git branch ft/branch

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git checkout -b ft/branch
fatal: a branch named 'ft/branch' already exists

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git switch ft/branch
Switched to branch 'ft/branch'

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/branch)
$ git add test5.md 

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/branch)
$ git commit -m "Implemented test 5"
[ft/branch 317deda] Implemented test 5
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test5.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/branch)
$ git checkout main
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 3 and 4 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git log
commit fcb8e48abc33c30c8987ef1824c8545148491a91 (HEAD -> main)
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:27:09 2025 +0200

    Create second file

commit 038c17c8a72aad7a0b564cc4bc817a50597de4b2
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 28 11:46:40 2025 +0200

    create third file

    create fourth file

commit 2e6f90bd2b095e27d3fb6a4a2d331d5ed841a55f
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:26:59 2025 +0200

:
commit fcb8e48abc33c30c8987ef1824c8545148491a91 (HEAD -> main)
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:27:09 2025 +0200

    Create second file

commit 038c17c8a72aad7a0b564cc4bc817a50597de4b2
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 28 11:46:40 2025 +0200

    create third file
    
    create fourth file

commit 2e6f90bd2b095e27d3fb6a4a2d331d5ed841a55f
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:26:59 2025 +0200


HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git swithch ft/branch
git: 'swithch' is not a git command. See 'git --help'.

The most similar command is
        switch

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git switch ft/branch
Switched to branch 'ft/branch'

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/branch)
$ git log
commit 317deda4114ee825d13771f6b93cc01b202b47c2 (HEAD -> ft/branch)
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Thu Jul 31 09:37:45 2025 +0200

    Implemented test 5

commit fcb8e48abc33c30c8987ef1824c8545148491a91 (main)
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 21 14:27:09 2025 +0200

    Create second file

commit 038c17c8a72aad7a0b564cc4bc817a50597de4b2
Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
Date:   Mon Jul 28 11:46:40 2025 +0200

    create third file


HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/branch)
$ git cherry-pick 317deda4114ee825d13771f6b93cc01b202b47c2
On branch ft/branch
You are currently cherry-picking commit 317deda.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

nothing to commit, working tree clean
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/branch|CHERRY-PICKING)
$ git --abort 
unknown option: --abort
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--no-lazy-fetch]   
           [--no-optional-locks] [--no-advice] [--bare] [--git-dir=<path>]
           [--work-tree=<path>] [--namespace=<name>] [--config-env=<name>=<envvar>]       
           <command> [<args>]

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/branch|CHERRY-PICKING)
$ git cherry-pick --skip

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/branch)
$ git log --oneline
317deda (HEAD -> ft/branch) Implemented test 5
fcb8e48 (main) Create second file
038c17c create third file
2e6f90b chore: Create initial file

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/branch)
$ git checkout main
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 3 and 4 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git cherry 317deda

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git cherry-pick 317deda
[main ac086c7] Implemented test 5
 Date: Thu Jul 31 09:37:45 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test5.md

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
```
Visualizing Commit History (Bonus):
```
HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git log --graph
* commit ac086c7c3e6233200127e636edae611f4431f64f (HEAD -> main)
| Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
| Date:   Thu Jul 31 09:37:45 2025 +0200
| 
|     Implemented test 5
|
* commit fcb8e48abc33c30c8987ef1824c8545148491a91
| Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
| Date:   Mon Jul 21 14:27:09 2025 +0200
|
|     Create second file
|
* commit 038c17c8a72aad7a0b564cc4bc817a50597de4b2
| Author: isaac benit <isaac.irakoze24snhu@keplercollege.ac.rw>
| Date:   Mon Jul 28 11:46:40 2025 +0200
|
|     create third file
|

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
```
Part 2 
Feature Branch Creation:
```
HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git branch ft/new-feature

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git switch ft/new-feature
Switched to branch 'ft/new-feature'

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/new-feature)
```
Working on the Feature Branch:
```
HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/new-feature)
$ git add feature.txt 

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/new-feature)
$ git commit -m 'Implemented core functionality for new feature'
[ft/new-feature bff1199] Implemented core functionality for new feature
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 feature.txt

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/new-feature)
```
Switching Back and Making More Changes:
```
HP-@isaacb24 MINGW64 /d/web/AdvancedGit (ft/new-feature)
$ git switch main
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 4 and 4 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git add readme.txt 

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
$ git commit -m 'Updated project readme'
[main 2d0ad47] Updated project readme
 1 file changed, 1 insertion(+)
 create mode 100644 readme.txt

HP-@isaacb24 MINGW64 /d/web/AdvancedGit (main)
```
