# Objetivo
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/238/atbash.jpg).
# Pistas
1. Download the image and try to extract it.
# Solución
```
ubuntu@ip-172-31-46-190:~/gio/hidetosee$ steghide extract -sf atbash.jpg
Enter passphrase:
wrote extracted data to "encrypted.txt".
ubuntu@ip-172-31-46-190:~/gio/hidetosee$ cat encrypted.txt
krxlXGU{zgyzhs_xizxp_8z0uvwwx}
picoCTF{atbash_crack_8a0feddc}
```
# Notas adicionales
# Referencias