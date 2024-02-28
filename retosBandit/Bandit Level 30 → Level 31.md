# Objetivo
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo` via the port `2220`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.
# Datos de acceso al nivel
username = bandit30
password = xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
# Solución
```
bandit30@bandit:~$ mktemp -d
/tmp/tmp.wWKaxlFVl5
bandit30@bandit:~$ cd /tmp/tmp.wWKaxlFVl5
bandit30@bandit:/tmp/tmp.wWKaxlFVl5$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit30/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit30/.ssh/known_hosts).
                         _                     _ _ _   
                        | |__   __ _ _ __   _| () |_ 
                        | '_ \ / ` | ' \ / _` | | __|
                        | |) | (| | | | | (| | | | 
                        |./ \,|| ||\,||\|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit30-git@localhost's password: 
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), done.
bandit30@bandit:/tmp/tmp.wWKaxlFVl5$ ls -la
total 408
drwx------    3 bandit30 bandit30   4096 Feb 28 05:12 .
drwxrwx-wt 1876 root     root     405504 Feb 28 05:13 ..
drwxrwxr-x    3 bandit30 bandit30   4096 Feb 28 05:12 repo
bandit30@bandit:/tmp/tmp.wWKaxlFVl5$ cd repo
bandit30@bandit:/tmp/tmp.wWKaxlFVl5/repo$ ls -la
total 16
drwxrwxr-x 3 bandit30 bandit30 4096 Feb 28 05:12 .
drwx------ 3 bandit30 bandit30 4096 Feb 28 05:12 ..
drwxrwxr-x 8 bandit30 bandit30 4096 Feb 28 05:12 .git
-rw-rw-r-- 1 bandit30 bandit30   30 Feb 28 05:12 README.md
bandit30@bandit:/tmp/tmp.wWKaxlFVl5/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.wWKaxlFVl5/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
bandit30@bandit:/tmp/tmp.wWKaxlFVl5/repo$ git tag
secret
bandit30@bandit:/tmp/tmp.wWKaxlFVl5/repo$ git shwo secret
git: 'shwo' is not a git command. See 'git --help'.

The most similar command is
        show
bandit30@bandit:/tmp/tmp.wWKaxlFVl5/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
```
# Notas adicionales
git show: para ver.
# Referencias