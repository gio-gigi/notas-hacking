# Objetivo
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/a350754a299cb58988d6d47aed5be3ba/Addadshashanammu.zip)
# Pistas
1. After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...
# Solución
```
giogi-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a350754a299cb58988d6d47aed5be3ba/Addadshashanammu.zip
--2024-03-03 21:22:31--  https://mercury.picoctf.net/static/a350754a299cb58988d6d47aed5be3ba/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4521 (4.4K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip'

Addadshashanammu.zip         100%[==============================================>]   4.42K  --.-KB/s    in 0s      

2024-03-03 21:22:31 (1.80 GB/s) - 'Addadshashanammu.zip' saved [4521/4521]

giogi-picoctf@webshell:~$ ls
Addadshashanammu.zip  README.txt  flag  flag.1  ltdis.sh  ltdis.sh.1  static  warm
giogi-picoctf@webshell:~$ unzip Addadshashanammu.zip
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
giogi-picoctf@webshell:~$ ls
Addadshashanammu  Addadshashanammu.zip  README.txt  flag  flag.1  ltdis.sh  ltdis.sh.1  static  warm
giogi-picoctf@webshell:~$ cd ^C
giogi-picoctf@webshell:~$ cd Addadshashanammu
giogi-picoctf@webshell:~/Addadshashanammu$ ls
Almurbalarammi
giogi-picoctf@webshell:~/Addadshashanammu$ cd Almurbalarammi
giogi-picoctf@webshell:~/Addadshashanammu/Almurbalarammi$ ls
Ashalmimilkala
giogi-picoctf@webshell:~/Addadshashanammu/Almurbalarammi$ cd Ashalmimilkala/
giogi-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala$ cd Assurnabitashpi/
giogi-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi$ cd Maelkashishi/Onnissiralis/
giogi-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis$ cd Ularradallaku/
giogi-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ul
arradallaku$ ls 
fang-of-haynekhtnamet
giogi-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ul
arradallaku$ strings fang-of-haynekhtnamet | grep picoCTF
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_a00cae70}
```
# Notas adicionales
- La importancia de los tabs.
# Referencias