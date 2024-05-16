# Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt).
# Pistas
1. As with most assembly, there is a lot of noise in the instruction dump. Find the one line that pertains to this question and don't second guess yourself!
# Solución

```
┌──(gio㉿kali)-[~/tercerparcial/bitoasm1]
└─$ cat disassembler-dump0_a.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x4],edi
<+11>:    mov    QWORD PTR [rbp-0x10],rsi
<+15>:    mov    eax,0x30
<+20>:    pop    rbp
<+21>:    ret

0x30 = 48
picoCTF{48}
```
# Notas adicionales
# Referencias
- https://decimal.info/hex-to-decimal/3/how-to-convert-0X30-to-decimal.html
