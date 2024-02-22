# Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

# Datos de acceso al nivel
username = bandit12
password = JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
# Solución
```
------------------------Solución dificil:-------------------------
bandit12@bandit:~$ xxd .profile -p
xxd: -p: Permission denied
bandit12@bandit:~$ xxd -r data.txt
�h44�z��A����@=�h4hh�␦␦␦��hd����������������9���1����������;,�
�����2�3d*58�~  �S�ZP^��luY��Br$�FP!%�s��h�?�)[=�h��O(B��2A���)�tZc��:�pã)�A�ˈ�0���΅A�yjeϢx,�(����z�E�+"�2�/�-��e"���^����t�j���$�d�@�dJơ'7\���$��m1c��#>�aԽ�EV��F��OCӐc@M�C���]��Y2^h8���D=��~        O�I��NDpF�+�|b#Jv�#�J��d�LފW$�Û�͖y�`
                                                                                                                    �\&��[�@*w�M�0θ��nr��C��`e$b�
                         ~�{���
                               ��`�<����a��?e:T���e�T4±b����)�@ِ���x=bandit12@bandit:~$
bandit12@bandit:~$ xxd -r data.txt | file -
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix
bandit12@bandit:~$ mkdir /tmp/37183708
bandit12@bandit:~$ cd /tmp/37183708
bandit12@bandit:/tmp/37183708$ xxd -r ~/data.txt > data
bandit12@bandit:/tmp/37183708$ ls
data
bandit12@bandit:/tmp/37183708$ file data
data: gzip compressed data, was "data2.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix, original size modulo 2^32 573
bandit12@bandit:/tmp/37183708$ mv data data.gz
bandit12@bandit:/tmp/37183708$ gzip -d data.gz
bandit12@bandit:/tmp/37183708$ ls
data
bandit12@bandit:/tmp/37183708$ file data
data: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/37183708$ mv data data.bz2
bandit12@bandit:/tmp/37183708$ ls
data.bz2
bandit12@bandit:/tmp/37183708$ bzip2 -d data.bz2
bandit12@bandit:/tmp/37183708$ ls
data
bandit12@bandit:/tmp/37183708$ file data
data: gzip compressed data, was "data4.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/37183708$ mv data data.gz
bandit12@bandit:/tmp/37183708$ ls
data.gz
bandit12@bandit:/tmp/37183708$ gzip -d data.gz
bandit12@bandit:/tmp/37183708$ ls
data
bandit12@bandit:/tmp/37183708$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/37183708$ mv data data.tar
bandit12@bandit:/tmp/37183708$ ls
data.tar
bandit12@bandit:/tmp/37183708$ tar xf data.tar
bandit12@bandit:/tmp/37183708$ ls
data5.bin  data.tar
bandit12@bandit:/tmp/37183708$ rm data.tar
bandit12@bandit:/tmp/37183708$ ls
data5.bin
bandit12@bandit:/tmp/37183708$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/37183708$ mv data5.bin data.tar
bandit12@bandit:/tmp/37183708$ ls
data.tar
bandit12@bandit:/tmp/37183708$ tar xf data.tar
bandit12@bandit:/tmp/37183708$ ls
data6.bin  data.tar
bandit12@bandit:/tmp/37183708$ rm data.tar
bandit12@bandit:/tmp/37183708$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/37183708$ mv data6.bin data6.bz2
bandit12@bandit:/tmp/37183708$ ls
data6.bz2
bandit12@bandit:/tmp/37183708$ file data6.bz2
data6.bz2: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/37183708$ bzip2 - d data6.bz2
bzip2: Can't open input file d: No such file or directory.
bzip2: Input file data6.bz2 already has .bz2 suffix.
bandit12@bandit:/tmp/37183708$ bzip2  d data6.bz2
bzip2: Can't open input file d: No such file or directory.
bzip2: Input file data6.bz2 already has .bz2 suffix.
bandit12@bandit:/tmp/37183708$ bzip2  -d data6.bz2
bandit12@bandit:/tmp/37183708$ ls
data6
bandit12@bandit:/tmp/37183708$ file data6
data6: POSIX tar archive (GNU)
bandit12@bandit:/tmp/37183708$ mv data6 data6.tar
bandit12@bandit:/tmp/37183708$ ls
data6.tar
bandit12@bandit:/tmp/37183708$ tar xf data6.tar
bandit12@bandit:/tmp/37183708$ ls
data6.tar  data8.bin
bandit12@bandit:/tmp/37183708$ rm data6.tar
bandit12@bandit:/tmp/37183708$ ls
data8.bin
bandit12@bandit:/tmp/37183708$ gzip -d data6.gz
gzip: data6.gz: No such file or directory
bandit12@bandit:/tmp/37183708$ gzip -d data8.gz
gzip: data8.gz: No such file or directory
bandit12@bandit:/tmp/37183708$ mv data8.bin data8.gz
bandit12@bandit:/tmp/37183708$ ls
data8.gz
bandit12@bandit:/tmp/37183708$ gzip -d data8.gz
bandit12@bandit:/tmp/37183708$ ls
data8
bandit12@bandit:/tmp/37183708$ file data8
data8: ASCII text
bandit12@bandit:/tmp/37183708$ car data8
Command 'car' not found, but can be installed with:
apt install ucommon-utils
Please ask your administrator.
bandit12@bandit:/tmp/37183708$ cat data8
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
-------SOLUCIÓN FACIL -------
bandit12@bandit:~$ xxd -r data.txt | file -
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat | file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar x0 | file -
tar: Options '-[0-7][lmh]' not supported by *this* tar
Try 'tar --help' or 'tar --usage' for more information.
/dev/stdin: empty
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat |file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | file -
/dev/stdin: gzip compressed data, was "data9.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file -
/dev/stdin: ASCII text
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

```
# Notas adicionales
whoami :
Es un vaciado hexadecimal : "00000000: 1f8b 0808 6855 1e65 0203 6461 7461 322e  ....hU.e..data2."
xxd : vaciar hexadecimal.
mv : mover o cambiar de nombre.
	.gz gzip -d    zcat
	.bz2  bzip2 -d  bzcat
	.tar    tar xf       tar xO
# Referencias