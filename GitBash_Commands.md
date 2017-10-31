First Commands in GitBash

1. Where am I??

Comand: pwd

2. what is the directory content?

Comand: ls

3. How to change my current working directory?

Comand: cd

*********************************************************************************
Example of 1, 2, 3:

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

4. How can I create a directory?

For example, the directory /c/github was created by using the command "mkdir". Ypu should code first the command "mkdir" and then the name of the directory 

*********************************************************************************
RodriguezJL@LT-RODRIGUEZJL MINGW64 /c

$ mkdir github
*********************************************************************************

5. How can I clone a directory from a repository of GitHub (Web)?

The directory /c/github/Learning-Python was created by using the command "got clone". You should code first the comand "git clone" and then the URL that is available when you choose a repository in GitHub.

*********************************************************************************
RodriguezJL@LT-RODRIGUEZJL MINGW64 /c/github

$ git clone https://github.com/Cyb3rPanda/Learning-Python.git

Cloning into 'Learning-Python'...
remote: Counting objects: 6, done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (6/6), done.
*********************************************************************************

6. Can I update files in my computer with changes that I made in the web?

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

