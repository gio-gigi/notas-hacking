# Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/511/disassembler-dump0_d.txt).
# Pistas
1. Don't tell anyone I told you this, but you can solve this problem without understanding the compare/jump relationship.
2. Of course, if you're really good, you'll only need one attempt to solve this problem.
# Solución
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
==<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a==   654874
==<+22>:    cmp    DWORD PTR [rbp-0x4],0x2710==
==<+29>:    jle    0x55555555514e <main+37>==
==<+31>:    sub    DWORD PTR [rbp-0x4],0x65==
==<+35>:    jmp    0x555555555152 <main+41>==
==<+37>:    add    DWORD PTR [rbp-0x4],0x65== resta 101
==<+41>:    mov    eax,DWORD PTR [rbp-0x4]==
<+44>:    pop    rbp
<+45>:    ret

```
0x9fe1a = 654874
0x65 = 101
654874 - 101 = 654773



picoCTF{654773}
```
# Notas adicionales
# Referencias
- https://www.rapidtables.com/convert/number/hex-to-decimal.html