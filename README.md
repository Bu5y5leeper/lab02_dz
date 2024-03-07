### lab02_dz
tp-lab02 homework

## Task2
```bash
git branch patch1
git status
```
```bash
On branch master
nothing to commit, working tree clean
bu5y@bu5y-virtual-machine:~/Bu5y5leeper/workspace/projects/lab02_dz$ git switch patch1
Switched to branch 'patch1'
bu5y@bu5y-virtual-machine:~/Bu5y5leeper/workspace/projects/lab02_dz$ git status
On branch patch1
nothing to commit, working tree clean
bu5y@bu5y-virtual-machine:~/Bu5y5leeper/workspace/projects/lab02_dz$ git status
On branch patch1
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   sources/hello_world.cpp

no changes added to commit (use "git add" and/or "git commit -a")
```

```bash
git add -A
git commit -m "codestyle improve"
```
```bash
[patch1 6335f5e] codestyle improve
 1 file changed, 3 insertions(+), 6 deletions(-)
```


```bash
git push origin patch1
```
```bash
Username for 'https://github.com': Bu5y5leeper
Password for 'https://Bu5y5leeper@github.com': 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 412 bytes | 137.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'patch1' on GitHub by visiting:
remote:      https://github.com/Bu5y5leeper/lab02_dz/pull/new/patch1
remote: 
To https://github.com/Bu5y5leeper/lab02_dz.git
 * [new branch]      patch1 -> patch1
```

```bash   
subl ./sources/hello_world.cpp 
git status
```
```bash
On branch patch1
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   sources/hello_world.cpp

no changes added to commit (use "git add" and/or "git commit -a")
```

```bash
git add -A
git commit -m "comments added"
```
```bash
[patch1 cb6d92f] comments added
 1 file changed, 3 insertions(+), 3 deletions(-)
bu5y@bu5y-virtual-machine:~/Bu5y5leeper/workspace/projects/lab02_dz$ git push origin patch1
Username for 'https://github.com': Bu5y5leeper
Password for 'https://Bu5y5leeper@github.com': 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 426 bytes | 142.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Bu5y5leeper/lab02_dz.git
   6335f5e..cb6d92f  patch1 -> patch1
bu5y@bu5y-virtual-machine:~/Bu5y5leeper/workspace/projects/lab02_dz$ git pull origin master
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 898 bytes | 449.00 KiB/s, done.
From https://github.com/Bu5y5leeper/lab02_dz
 * branch            master     -> FETCH_HEAD
   2005073..6ffe733  master     -> origin/master
Updating cb6d92f..6ffe733
Fast-forward
```

```bash
git log
```
```bash
commit 6ffe733a4910840edc311799cc2f2810208f36e8 (HEAD -> patch1, origin/master)
Merge: 2005073 cb6d92f
Author: Bu5y5leeper <132168412+Bu5y5leeper@users.noreply.github.com>
Date:   Thu Mar 7 09:57:04 2024 +0300

    Merge pull request #1 from Bu5y5leeper/patch1
    
    codestyle improve

commit cb6d92f8cc0ad78417c35bd3d105608067e901e2 (origin/patch1)
Author: Bu5y5leeper <studpack@yandex.ru>
Date:   Thu Mar 7 09:56:21 2024 +0300

    comments added

commit 6ffe733a4910840edc311799cc2f2810208f36e8 (HEAD -> patch1, origin/master)
Merge: 2005073 cb6d92f
Author: Bu5y5leeper <132168412+Bu5y5leeper@users.noreply.github.com>
Date:   Thu Mar 7 09:57:04 2024 +0300

    Merge pull request #1 from Bu5y5leeper/patch1
    
    codestyle improve

commit cb6d92f8cc0ad78417c35bd3d105608067e901e2 (origin/patch1)
Author: Bu5y5leeper <studpack@yandex.ru>
Date:   Thu Mar 7 09:56:21 2024 +0300

    comments added

commit 6335f5e3871c67643561b6048791c949c77dcb26
Author: Bu5y5leeper <studpack@yandex.ru>
Date:   Thu Mar 7 09:51:58 2024 +0300

    codestyle improve

commit 2005073289471c3c0737325f70ceacbb357675e9 (master)
Author: Bu5y5leeper <studpack@yandex.ru>

[1]+  Stopped                 git log
```

## Task3

```bash
git branch patch2
git status
```
```bash
On branch patch2
nothing to commit, working tree clean
```

```bash
clang-format -style=Mozilla ./sources/hello_world.cpp
```
```bash 
#include <iostream>
#include <string>

int
main()
{
  string name;                                // name
  std::cin >> name;                           // input
  std::cout << "hello from " << name << endl; // output
  return 0;
}
clang-format -i ./sources/hello_world.cpp 
```

```bash
git add -A
git commit -m "mozilla codestyle"
```
```bash
[patch2 0f809f7] mozilla codestyle
 1 file changed, 4 insertions(+), 4 deletions(-)
```

```bash
git push origin patch2
```
```bash
Username for 'https://github.com': Bu5y5leeper
Password for 'https://Bu5y5leeper@github.com': 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 428 bytes | 214.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'patch2' on GitHub by visiting:
remote:      https://github.com/Bu5y5leeper/lab02_dz/pull/new/patch2
remote: 
To https://github.com/Bu5y5leeper/lab02_dz.git
 * [new branch]      patch2 -> patch2
```

```bash
git pull origin master
```
```bash
remote: Enumerating objects: 7, done.
remote: Counting objects: 100% (7/7), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 4 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), 1015 bytes | 126.00 KiB/s, done.
From https://github.com/Bu5y5leeper/lab02_dz
 * branch            master     -> FETCH_HEAD
   36e0089..c673f18  master     -> origin/master
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint: 
hint:   git config pull.rebase false  # merge (the default strategy)
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint: 
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.
```

```bash
git pull --rebase origin master
```
```bash
From https://github.com/Bu5y5leeper/lab02_dz
 * branch            master     -> FETCH_HEAD
warning: skipped previously applied commit 0bd2faf
warning: skipped previously applied commit 8470088
hint: use --reapply-cherry-picks to include skipped commits
hint: Disable this message with "git config advice.skippedCherryPicks false"
Auto-merging sources/hello_world.cpp
CONFLICT (content): Merge conflict in sources/hello_world.cpp
error: could not apply b501ff9... mozilla codestyle
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
Could not apply b501ff9... mozilla codestyle
```

```bash
git rebase --continue
```
```bash
[detached HEAD 99ef06e] mozilla codestyle rebase
 1 file changed, 7 insertions(+)
Successfully rebased and updated refs/heads/patch2.
```

```bash
git push origin patch2 --force
```
```bash
Username for 'https://github.com': Bu5y5leeper
Password for 'https://Bu5y5leeper@github.com': 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 504 bytes | 168.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Bu5y5leeper/lab02_dz.git
 + b501ff9...99ef06e patch2 -> patch2 (forced update)
```
