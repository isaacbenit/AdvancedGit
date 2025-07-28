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
