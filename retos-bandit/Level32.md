# Level 32

## Objetivos
There is a git repository at `ssh://bandit31-git@localhost/home/bandit31-git/repo`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

Clone the repository and find the password for the next level.

## Datos de acceso 
bandit31 <-UserName
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt <-Password
## Solución 
```bash
bandit31@bandit:~$ mkdir /tmp/vis/
bandit31@bandit:~$ cd /tmp/vis
bandit31@bandit:/tmp/vis$ git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo
Cloning into 'repo'...
bandit31@bandit:/tmp/vis$ ls
repo
bandit31@bandit:/tmp/vis$ cd repo
bandit31@bandit:/tmp/visrepo$ ls
README.md
bandit31@bandit:/tmp/vis/repo$ cat README.md
This time your task is to push a file to the remote repository.
Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master
bandit31@bandit:/tmp/vis/repo$ echo 'May I come in?' > key.txt
bandit31@bandit:/tmp/vis/repo$ cat key.txt
May I come in?
bandit31@bandit:/tmp/vis/repo$ git add key.txt
The following paths are ignored by one of your .gitignore files:
key.txt
hint: Use -f if you really want to add them.
hint: Turn this message off by running
hint: "git config advice.addIgnoredFile false"
bandit31@bandit:/tmp/vis/repo$ git add -f key.txt
bandit31@bandit:/tmp/vis/repo$ git commit -m "task"
[master 53c9dd5] task
 1 file changed, 1 insertion(+)
 create mode 100644 key.txt
bandit31@bandit:/tmp/vis/repo$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 319 bytes | 319.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)

bandit31@bandit:/tmp/nuevo/repo$
```

## Notas dicionales