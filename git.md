# GIT

1.  **Intializing**

    - initialize git

      `git init`

2.  **Configuring**

    - configuring name

      `git config --global user.name "Ehsaan"`

    * configuring email

      `git config --global user.email ehsaan.qazi.1337@gmail.com`

    * configuring editor

      `git config --global core.editor "code --wait"`

    * configuring command line color

      `git config --global color.ui auto`

    - configure merge tool

      `git config -g merge.tool toolname`

    - configuring diff tool

      `git config --global diff.tool vscode (naming our default diff tool`

    * open the editor with the git configuration file

      `git config --global-e`

    * remove carriage returns

      `git config --global core.autocrlf input(windows) or true(mac/linux)`

    * displays the help menu

      `git config --help`

    * quick help

      `git config --h`

    * configure how to launch vscode

      `git config --global difftool.vscode.cmd = "code --wait --diff $LOCAL $REMOTE"`

    * configuring aliases

      `git config --global alias.s "status -s"`

    * disable fast forward merge for local repository

      `git config ff no`

    * disable fast forward merge globally

      `git config --global ff no`

    * storing credentials

      `git config --global credential.helper osxkeychain`

    - ignore patterns

      `git config --global core.excludesfile file`

    - display current config

      `git config --list`

    - display repo config

      `git config --local --list`

    - display system config

      `git config --system --list`

3.  **Staging**

    - add file to staging area

      `git add file.txt`

    - add multiple files to staging area

      `git add file.txt file1.txt`

    - add all files to staging area

      `git add .`

    - add pattern of files

      `git add \*.txt`

    - remove all files from staging area

      `git reset HEAD`

    - display files in staging area

      `git ls-files`

    - remove file from staging area and from working directory

      `git rm file.txt`

    - move files from working directory and staging area

      `git mv file.txt`

    - view staged changes

      `git diff --staged`

    - view staged changes in diff tool

      `git difftool --staged`

    * unstage file

      `git restore --staged file.txt`

4.  **Commit**

    - commit changes

      `git commit -m "commit message"`

    * skip staging area and directly commit

      `git commit -am "commit message"`

    * commit message with title and description

      `git commit -m "Title" -m "Description..."`

    * commit all local changes

      `git commit -a`

    * commit message with description

      `git commit -m "Initial Commit" -m "Description"`

    * view commit

      `git show`

    * viewing specific commit

      `git show commitID`

    * viewing all files in commit

      `git ls-tree HEAD~1`

    * view the earlier version of code

      `git checkout commit`

    * view all commits also with the hidden commits

      `git log --oneline --all`

    * Ammending last commit

      `git commit --amend`

    * skip ammending published commits

      `git commit --amend --no-edit`

5.  **Filtering History**

    - The command will show only last 3 commits

      `git log --oneline -3`

    - The command will filter the history by author name

      `git log --oneline --author="Ehsaan"`

    * The command will filter by date

      `git log --oneline --before="2021-04-2"`

      `git log --oneline --after="2021-04-2"`

    * The command will filter by relative dates

      `git log --oneline --after="yesterday"`

      `git log --oneline --after="one week ago"`

    - The command will filter by commit message

      `git log --oneline --grep="fixed scroll"`

    - The command will filter by any code

      `git log --oneline -S"start()"`

    - The command will filter by any code and preview the changes

      `git log --oneline -S"start()" --patch`

    - The command will get data from range of commits

      `git log --oneline commit1..commit2`

    - The command will preview the commits that have modified the particular file

      `git log --oneline file1.txt`

    - The command will preview the commits that have modified the particular file with the changes previewed

      `git log --oneline --patch file1.txt`

6.  **Removing and Moving files**

    - remove files from working directory and staged area

      `git rm file.txt`

    - remove multiple files from working directory and staged area

      `git rm file.txt file2.txt`

    - remove pattern of files from working directory and staged area

      `git rm \*.js`

    - move files

      `git mv file.txt`

      `git mv file.txt file1.txt`

      `git mv \*.js`

    * rename files

      `git mv file.txt file.js`

    - ignore the file already in staged area

      `git rm --cached file.txt`

    - remove files that were committed before they were added to .gitignore

      `git rm -r --cached .`

    * change an existing file path

      `git mv [existingPath] [newPath]`

7.  **Branches**

    - list all branches

      `git branch`

    * list all merged branches

      `git branch --merged`

    * list all unmerged branches

      `git branch --unmerged`

    * list remote branches

      `git branch -r`

    * list local as well as remote branches

      `git branch -a`

    * create a new branch

      `git branch auth`

    * switch to a branch

      `git switch auth`

    * rename branch

      `git switch -m auth authentication`

    * delete branch

      `git brach -d auth`

    * forcefully delete a branch

      `git branch -D auth`

8.  **Merging**

    - merge with fast forward

      `git merge auth`

    - create and switch to new branch

      `git switch -C auth`

    * defines no fast forward merge

      `git merge --no-ff auth`

    * merge only if fast forward

      `git merge --ff-only auth`

    - merge with 3 way merge

      `git merge auth`

    - merge with squash merging

      `git merge --squash auth`

    - aborting a merge

      `git merge --abort`

    - reset changes in working directory, staging area and also in last snapshot

      `git reset --hard HEAD~1`

    * use merge tool to solve conflicts

      `git mergetool`

9.  **Diff Commands**

    - view unstaged changes

      `git diff`

    * view staged changes

      `git diff --staged`

    * view staged changes in difftool

      `git difftool`

    * view unstaged changes in difftool

      `git difftool --staged`

    * show changes between two commits

      `git diff HEAD~2 HEAD`

    * show changes of the specified filename

      `git diff HEAD~2 HEAD test.js`

    * show file name only

      `git diff HEAD~2 HEAD --name-only`

    * show file with status

      `git diff HEAD~2 --name-status`

    * diff between branches

      `git diff one..two`

    * compare modified files and display changes

      `git diff --color-words file.js`

    * compare commits

      `git diff commitID..commitID`

10. **Tagging**

    - list tags

      `git tag`

    * create a tag

      `git tag v1.0 commitid`

    - create tag with comment

      `git tag -a v1.0.0 -m 'Message'`

    - annoted tags

      `git tag -a v2.0 "Version 2.0"`

    - display all tags

      `git tag`

    - display all tags with message

      `git tag -n`

    - display all released versions

      `git tag -l -n1`

11. **Stashing**

    - create a stash

      `git stash push -m "I_am_Coder"`

    * create a stash with a file included

      `git stash push -am "stash"`

    * list stashes

      `git stash list`

    * show changes in a stash

      `git stash show`

    * apply stash to working directory

      `git stash apply`

    * remove stash

      `git stash drop 0`

    * remove all stash

      `git stash clear`

12. **Short Logs**

    - display shortlog

      `git shortlog`

    - author with highest commits

      `git shortlog -n`

    * most number of commited author with displaying number of commits

      `git shortlog -n -s`

    * most number of commited author with displaying number of commits and email

      `git shortlog -n -s -e`

    * most number of commited author with displaying number of commits and email withing date range

      `git shortlog -n -s -before || --after`

13. **Blame**

    - showing all commits

      `git blame file.js`

    * showing commits with email

      `git blame -e file.js`

    * show limited number of commits (3 commits)

      `git blame -e -L 1,3 file.js`

14. **Extra Commands**

    - show modified files

      `git status`

    * short status

      `git status -s`

    * clone a repository

      `git clone url`

    * clone repository with new name

      `git clone url repoNewName`

    * clone repo via ssh

      `git clone ssh://admin@ehsaanqazi.com/blog.git`

    * clone a branch name

      `git clone -b branchname url`

    * display remote repo

      `git remote`

    * display deatils about remote repo

      `git remote -v`

    * download commits

      `git fetch`

    * pull by 3 way merge

      `git pull`

    * pull by rebassing

      `git pull --rebase`

    * push to remote

      `git push`

    * force push

      `git push --force`

    * add tag to the repo

      `git push origin tagname`

    * delete tag from repo

      `git push origin --delete tagname`

    - push branch name to origin

      `git push -u origin branchname`

    * delete branch name from origin

      `git push -d origin branchname`

    * display help menu

      `git help`
