# Objetivo
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it.Download the data [here](https://artifacts.picoctf.net/c/124/anthem.flag.txt).
# Pistas
1. Download the file and search for the flag based on the known prefix.
# Solución
```
┌──(gio㉿kali)-[~/picoctf/forensic/lookeyhere]
└─$ ls
anthem.flag.txt
                                                                                                      
┌──(gio㉿kali)-[~/picoctf/forensic/lookeyhere]
└─$ open anthem.flag.txt 
                                                                                                      
┌──(gio㉿kali)-[~/picoctf/forensic/lookeyhere]
└─$ strings anthem.flag.txt | grep pico       
      we think that the men of picoCTF{gr3p_15_@w3s0m3_4c479940}
```
# Notas adicionales
# Referencias