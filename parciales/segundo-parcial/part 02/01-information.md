# Objetivo
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/149ab4b27d16922142a1e8381677d76f/cat.jpg)
# Pistas
# Solución
```
┌──(gio㉿kali)-[~/picoctf/forensic/information]
└─$ open cat.jpg 
                                                                                                      
┌──(gio㉿kali)-[~/picoctf/forensic/information]
└─$ file cat.jpg     
cat.jpg: JPEG image data, JFIF standard 1.02, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 2560x1598, components 3
                                                                                                      
┌──(gio㉿kali)-[~/picoctf/forensic/information]
└─$ binwalk cat.jpg          

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             JPEG image data, JFIF standard 1.02

                                                                                                      
┌──(gio㉿kali)-[~/picoctf/forensic/information]
└─$ strings cat.jpg | grep pico                             
                                                                                                      
┌──(gio㉿kali)-[~/picoctf/forensic/information]
└─$ hexeditor cat.jpg

cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
picoCTF{the_m3tadata_1s_modified}
```
# Notas adicionales
# Referencias
https://www.base64decode.org/