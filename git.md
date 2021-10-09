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
