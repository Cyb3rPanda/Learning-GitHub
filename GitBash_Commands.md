First Commands in GitBash

** 1. Where am I??

Comand: pwd

2. what is the directory content?

Comand: ls

3. How to change my current working directory?

Comand: cd

*********************************************************************************
** Example of 1, 2, 3:

RodriguezJL@LT-RODRIGUEZJL MINGW64 /

$ pwd

/

RodriguezJL@LT-RODRIGUEZJL MINGW64 /

$ ls

bin/  etc/           LICENSE.txt  ReleaseNotes.html  unins000.exe*
cmd/  git-bash.exe*  mingw64/     tmp/               unins000.msg
dev/  git-cmd.exe*   proc/        unins000.dat       usr/

RodriguezJL@LT-RODRIGUEZJL MINGW64 /

$ cd /c/github/

RodriguezJL@LT-RODRIGUEZJL MINGW64 /c/github

$ ls

how_to_create_a_new_repository_git_hub.docx  Learning-GitHub/  Learning-Python/

RodriguezJL@LT-RODRIGUEZJL MINGW64 /c/github

$ cd Learning-GitHub/

RodriguezJL@LT-RODRIGUEZJL MINGW64 /c/github/Learning-GitHub (master)
$

*********************************************************************************

** 4. How can I create a directory?

For example, the directory /c/github was created by using the command "mkdir". You should code first the command "mkdir" and then the name of the directory 

*********************************************************************************
RodriguezJL@LT-RODRIGUEZJL MINGW64 /c

$ mkdir github
*********************************************************************************

** 5. How can I clone a directory from a repository of GitHub (Web)?

The directory /c/github/Learning-Python was created by using the command "git clone". You should code first the comand "git clone" and then the URL that is available when you choose a repository in GitHub.

*********************************************************************************
RodriguezJL@LT-RODRIGUEZJL MINGW64 /c/github

$ git clone https://github.com/Cyb3rPanda/Learning-Python.git

Cloning into 'Learning-Python'...
remote: Counting objects: 6, done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (6/6), done.
*********************************************************************************

** 6. Can I update files in my computer with changes that I made in the web?

This option is available using the command "git pull". To use this command is neccessary that your current working directory would be the cloned repository from GitHub. 

*********************************************************************************
RodriguezJL@LT-RODRIGUEZJL MINGW64 /c/github/Learning-GitHub (master)

$ git pull

remote: Counting objects: 11, done.
remote: Compressing objects: 100% (10/10), done.
remote: Total 11 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (11/11), done.
From https://github.com/Cyb3rPanda/Learning-GitHub
   bd90e6a..afff13f  master     -> origin/master
Updating bd90e6a..afff13f
Fast-forward
 GitBash.ipynb       |  2 --
 GitBash_Commands.md | 34 ++++++++++++++++++++++++++++++++++
 2 files changed, 34 insertions(+), 2 deletions(-)
 delete mode 100644 GitBash.ipynb
 create mode 100644 GitBash_Commands.md
*********************************************************************************

** 7. Can I update files in the web with changes that I made in my computer?

At the first time you try to update your files in the web, its important to config the user name and user mail of GitHub. The commands to config the user and the mail are " git config --global user.name "user_example" " and " git config --global user.mail "example@gmail" "

after config your user and mail, yoy need to use these commands "git add -A", " git commit -m "example of comment" " and "git push"

*********************************************************************************
RodriguezJL@LT-RODRIGUEZJL MINGW64 /c/github/Learning-Python (master)

$ git config --global user.name "user_example"

RodriguezJL@LT-RODRIGUEZJL MINGW64 /c/github/Learning-Python (master)

$ git config --global user.email example@gmail

RodriguezJL@LT-RODRIGUEZJL MINGW64 /c/github/Learning-Python (master)

$ git add -A

RodriguezJL@LT-RODRIGUEZJL MINGW64 /c/github/Learning-Python (master)

$ git commit -m "Comment example"

On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

RodriguezJL@LT-RODRIGUEZJL MINGW64 /c/github/Learning-Python (master)

$ git push

Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.69 KiB | 863.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/Cyb3rPanda/Learning-Python.git
   eb781d8..7dc575c  master -> master

RodriguezJL@LT-RODRIGUEZJL MINGW64 /c/github/Learning-Python (master)
$

*********************************************************************************
** 8. Can I update my files with jupyter notebook?

First, you need to install Jupyter. You can install jupyter by using Anaconda (https://www.anaconda.com/download/#windows).
Be sure of check the Path option during the installation process. I know that it is not a recommended option, but it is necesary to use the jupyter notebook comand in PowerShell/Terminal/Bash.

After you install Anaconda in your computer, you should code "jupyter notebokk" in PowerShell/Terminal/Bash and it will open an internet window with Jupyter. Before you code "jupyter notebook", you must use the comand "cd" (Change Directoy) to set the working directory you want to manage by jupyter.

*********************************************************************************
** For example, I want to manage my Github files that i just clone in my computer:

Robert@Robert-PC MINGW64 /
$ pwd
/

Robert@Robert-PC MINGW64 /
$ ls
bin/  dev/  git-bash.exe*  LICENSE.txt  proc/              tmp/          unins000.exe*  usr/
cmd/  etc/  git-cmd.exe*   mingw64/     ReleaseNotes.html  unins000.dat  unins000.msg

Robert@Robert-PC MINGW64 /
$ cd /c/

Robert@Robert-PC MINGW64 /c
$ ls
'$RECYCLE.BIN'/             Drivers/       PerfLogs/                     tools/
 Apps/                      Github/       'Program Files'/               Uploads/
 Captures/                  hiberfil.sys  'Program Files (x86)'/         Users/
 DELL/                      Intel/         ProgramData/                  WINDOWS/
 dell.sdr                   java/         'System Volume Information'/
'Documents and Settings'@   pagefile.sys   Temp/

Robert@Robert-PC MINGW64 /c
$ cd Github

Robert@Robert-PC MINGW64 /c/Github

**After that, you can code "jupyter notebook"

Robert@Robert-PC MINGW64 /c/Github
$ jupyter notebook

[I 06:38:23.500 NotebookApp] JupyterLab alpha preview extension loaded from C:\Users\Robert\Anaconda3\lib\site-packages\jupyterlab
JupyterLab v0.27.0
Known labextensions:
[I 06:38:23.502 NotebookApp] Running the core application with no additional extensions or settings
[I 06:38:23.714 NotebookApp] Serving notebooks from local directory: C:\Github
[I 06:38:23.714 NotebookApp] 0 active kernels
[I 06:38:23.714 NotebookApp] The Jupyter Notebook is running at: http://localhost:8888/?token=5ff49bc384e1e5a05ce77aaa9fa1b00ecc29d721f8519ea9
[I 06:38:23.714 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 06:38:23.716 NotebookApp]

    Copy/paste this URL into your browser when you connect for the first time,
    to login with a token:
        http://localhost:8888/?token=5ff49bc384e1e5a05ce77aaa9fa1b00ecc29d721f8519ea9
[I 06:38:23.762 NotebookApp] Accepting one-time-token-authenticated connection from ::1
[I 06:43:54.882 NotebookApp] Creating new file in /Learning-GitHub

*********************************************************************************


