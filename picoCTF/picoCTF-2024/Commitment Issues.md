## Objetivo
I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/136/challenge.zip)
## Solución

```
vagrant@ubuntu-jammy:~$ ls
challenge.zip  drop-in
vagrant@ubuntu-jammy:~$ cd drop-in/
vagrant@ubuntu-jammy:~/drop-in$ ls
message.txt
vagrant@ubuntu-jammy:~/drop-in$ cat message.txt
TOP SECRET
vagrant@ubuntu-jammy:~/drop-in$ git log
commit 8dc51806c760dfdbb34b33a2008926d3d8e8ad49 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:17 2024 +0000

    remove sensitive info

commit 87b85d7dfb839b077678611280fa023d76e017b8
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:17 2024 +0000

    create flag

vagrant@ubuntu-jammy:~/drop-in$ git checkout 87b85d7dfb839b077678611280fa023d76e017b8
Previous HEAD position was 8dc5180 remove sensitive info
HEAD is now at 87b85d7 create flag
vagrant@ubuntu-jammy:~/drop-in$ ls
message.txt
vagrant@ubuntu-jammy:~/drop-in$ cat message.txt
picoCTF{s@n1t1z3_ea83ff2a}
vagrant@ubuntu-jammy:~/drop-in$
```
## Notas adicionales
## Referencias