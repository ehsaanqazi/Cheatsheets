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
