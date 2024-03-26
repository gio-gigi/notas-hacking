## Objetivo
Know of little and big endian? `nc titan.picoctf.net 65205`. [Source](https://artifacts.picoctf.net/c_titan/119/flag.c)
## Pistas
### 1
You might want to check the ASCII table to first find the hexadecimal representation of characters before finding the endianness.
### 2
Read more about how endianness [here](https://levelup.gitconnected.com/little-endian-and-big-endian-74ab6441b2a7)
## Solución
```
┌──(rio11㉿kali)-[~/Downloads]
└─$ nc titan.picoctf.net 49546        
Welcome to the Endian CTF!
You need to find both the little endian and big endian representations of a word.
If you get both correct, you will receive the flag.
Word: zlgpc
Enter the Little Endian representation: 6370676C7A
Correct Little Endian representation!
Enter the Big Endian representation: 7A6C677063
Correct Big Endian representation!
Congratulations! You found both endian representations correctly!
Your Flag is: picoCTF{3ndi4n_sw4p_su33ess_28329f0a}
```
## Bandera Obtenida
picoCTF{3ndi4n_sw4p_su33ess_28329f0a}
## Notas adicionales
Primero tenemos que convertir las letras en formato hexadecimal y despues tranformarlo a Little Endian y cuando este aprobada lo pasas en formato Big Endian
## Referencias
https://www.save-editor.com/tools/wse_hex.html
https://gchq.github.io/CyberChef/