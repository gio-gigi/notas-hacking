# Objetivo
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/29b91e638ccbd76aaa8c0462d1c64d8d/VaultDoor1.java)
# Pistas
1. Look up the charAt() method online.
# Solución
```
cat flag | sort 

cat flag | sort | awk '{print $3}'
'3'
'5'
'c'
'r'
'4'
'm'
┌──(gio㉿kali)-[~/picoctf/reversing/vaultdoor1]
└─$ cat flag | sort | awk '{print $3}' | tr -d "'"
3
5
c

┌──(gio㉿kali)-[~/picoctf/reversing/vaultdoor1]
└─$ cat flag | sort | awk '{print $3}' | tr -d "'" | tr -d "\n"
d35cr4mbl3_tH3_cH4r4cT3r5_ff63b0  
```

```
picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_ff63b0}
```
# Notas adicionales
- awk:  Procesamiento 
# Referencias