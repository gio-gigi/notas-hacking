
# Objetivo
Can you get the flag?Download this [binary](https://artifacts.picoctf.net/c/87/gdbme).Here's the test drive instructions:

- `$ chmod +x gdbme`
- `$ gdb gdbme`
- `(gdb) layout asm`
- `(gdb) break *(main+99)`
- `(gdb) run`
- `(gdb) jump *(main+104)`
# Pistas
none
# Solución
```
gdb -q
(gdb) quit
	info functions
	run 
	(gdb) disassemble main
Dump of assembler code for function main:
   0x00005555555552c7 <+0>:     endbr64
   0x00005555555552cb <+4>:     push   %rbp
   0x00005555555552cc <+5>:     mov    %rsp,%rbp
   0x00005555555552cf <+8>:     sub    $0x50,%rsp
   0x00005555555552d3 <+12>:    mov    %edi,-0x44(%rbp)
   0x00005555555552d6 <+15>:    mov    %rsi,-0x50(%rbp)
   0x00005555555552da <+19>:    mov    %fs:0x28,%rax
   0x00005555555552e3 <+28>:    mov    %rax,-0x8(%rbp)
   0x00005555555552e7 <+32>:    xor    %eax,%eax
   0x00005555555552e9 <+34>:    movabs $0x4c75257240343a41,%rax
   0x00005555555552f3 <+44>:    movabs $0x4362383846336235,%rdx
   0x00005555555552fd <+54>:    mov    %rax,-0x30(%rbp)
   0x0000555555555301 <+58>:    mov    %rdx,-0x28(%rbp)
   0x0000555555555305 <+62>:    movabs $0x6630624760433530,%rax
   0x000055555555530f <+72>:    movabs $0x4e67646635656666,%rdx
   0x0000555555555319 <+82>:    mov    %rax,-0x20(%rbp)
   0x000055555555531d <+86>:    mov    %rdx,-0x18(%rbp)
   0x0000555555555321 <+90>:    movb   $0x0,-0x10(%rbp)
   0x0000555555555325 <+94>:    mov    $0x186a0,%edi
   0x000055555555532a <+99>:    call   0x555555555110 <sleep@plt>
   0x000055555555532f <+104>:   lea    -0x30(%rbp),%rax
   0x0000555555555333 <+108>:   mov    %rax,%rsi
   0x0000555555555336 <+111>:   mov    $0x0,%edi
   0x000055555555533b <+116>:   call   0x555555555209 <rotate_encrypt>
   0x0000555555555340 <+121>:   mov    %rax,-0x38(%rbp)
   ------------------------------------------------------
   (gdb) disassemble main
   (gdb) break *(main+99)
   (gdb) run 
   (gdb) jump *(main+104)
```

```
picoCTF{d3bugg3r_dr1v3_7776d758}
```
# Notas adicionales
gdb -q : entramos sin que nos muestre el banner
	- quit: para salir de gdb
# Referencias