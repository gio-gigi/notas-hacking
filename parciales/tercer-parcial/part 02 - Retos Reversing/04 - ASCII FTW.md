# Objetivo
This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program.You can download the file from [here](https://artifacts.picoctf.net/c/507/asciiftw).
# Pistas
1. The combined range of hex-ascii for English alphabets and numerical digits is from 30 to 7A.
2. Online hex-ascii converters can be helpful.
# Solución

```
┌──(gio㉿kali)-[~/tercerparcial/asciiftw]
└─$ objdump -d asciiftw > disassembled_asciiftw.txt
                                                                             
┌──(gio㉿kali)-[~/tercerparcial/asciiftw]
└─$ cat disassembled_asciiftw.txt | grep "<main>:" -A 40
0000000000001169 <main>:
    1169:       f3 0f 1e fa             endbr64
    116d:       55                      push   %rbp
    116e:       48 89 e5                mov    %rsp,%rbp
    1171:       48 83 ec 30             sub    $0x30,%rsp
    1175:       64 48 8b 04 25 28 00    mov    %fs:0x28,%rax
    117c:       00 00 
    117e:       48 89 45 f8             mov    %rax,-0x8(%rbp)
    1182:       31 c0                   xor    %eax,%eax
    1184:       c6 45 d0 70             movb   $0x70,-0x30(%rbp)
    1188:       c6 45 d1 69             movb   $0x69,-0x2f(%rbp)
    118c:       c6 45 d2 63             movb   $0x63,-0x2e(%rbp)
    1190:       c6 45 d3 6f             movb   $0x6f,-0x2d(%rbp)
    1194:       c6 45 d4 43             movb   $0x43,-0x2c(%rbp)
    1198:       c6 45 d5 54             movb   $0x54,-0x2b(%rbp)
    119c:       c6 45 d6 46             movb   $0x46,-0x2a(%rbp)
    11a0:       c6 45 d7 7b             movb   $0x7b,-0x29(%rbp)
    11a4:       c6 45 d8 41             movb   $0x41,-0x28(%rbp)
    11a8:       c6 45 d9 53             movb   $0x53,-0x27(%rbp)
    11ac:       c6 45 da 43             movb   $0x43,-0x26(%rbp)
    11b0:       c6 45 db 49             movb   $0x49,-0x25(%rbp)
    11b4:       c6 45 dc 49             movb   $0x49,-0x24(%rbp)
    11b8:       c6 45 dd 5f             movb   $0x5f,-0x23(%rbp)
    11bc:       c6 45 de 49             movb   $0x49,-0x22(%rbp)
    11c0:       c6 45 df 53             movb   $0x53,-0x21(%rbp)
    11c4:       c6 45 e0 5f             movb   $0x5f,-0x20(%rbp)
    11c8:       c6 45 e1 45             movb   $0x45,-0x1f(%rbp)
    11cc:       c6 45 e2 41             movb   $0x41,-0x1e(%rbp)
    11d0:       c6 45 e3 53             movb   $0x53,-0x1d(%rbp)
    11d4:       c6 45 e4 59             movb   $0x59,-0x1c(%rbp)
    11d8:       c6 45 e5 5f             movb   $0x5f,-0x1b(%rbp)
    11dc:       c6 45 e6 37             movb   $0x37,-0x1a(%rbp)
    11e0:       c6 45 e7 42             movb   $0x42,-0x19(%rbp)
    11e4:       c6 45 e8 43             movb   $0x43,-0x18(%rbp)
    11e8:       c6 45 e9 44             movb   $0x44,-0x17(%rbp)
    11ec:       c6 45 ea 39             movb   $0x39,-0x16(%rbp)
    11f0:       c6 45 eb 37             movb   $0x37,-0x15(%rbp)
    11f4:       c6 45 ec 31             movb   $0x31,-0x14(%rbp)
    11f8:       c6 45 ed 44             movb   $0x44,-0x13(%rbp)
    11fc:       c6 45 ee 7d             movb   $0x7d,-0x12(%rbp)
    1200:       0f b6 45 d0             movzbl -0x30(%rbp),%eax
                                                                             
┌──(gio㉿kali)-[~/tercerparcial/asciiftw]
└─$ cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb
    1184:       c6 45 d0 70             movb   $0x70,-0x30(%rbp)
    1188:       c6 45 d1 69             movb   $0x69,-0x2f(%rbp)
    118c:       c6 45 d2 63             movb   $0x63,-0x2e(%rbp)
    1190:       c6 45 d3 6f             movb   $0x6f,-0x2d(%rbp)
    1194:       c6 45 d4 43             movb   $0x43,-0x2c(%rbp)
    1198:       c6 45 d5 54             movb   $0x54,-0x2b(%rbp)
    119c:       c6 45 d6 46             movb   $0x46,-0x2a(%rbp)
    11a0:       c6 45 d7 7b             movb   $0x7b,-0x29(%rbp)
    11a4:       c6 45 d8 41             movb   $0x41,-0x28(%rbp)
    11a8:       c6 45 d9 53             movb   $0x53,-0x27(%rbp)
    11ac:       c6 45 da 43             movb   $0x43,-0x26(%rbp)
    11b0:       c6 45 db 49             movb   $0x49,-0x25(%rbp)
    11b4:       c6 45 dc 49             movb   $0x49,-0x24(%rbp)
    11b8:       c6 45 dd 5f             movb   $0x5f,-0x23(%rbp)
    11bc:       c6 45 de 49             movb   $0x49,-0x22(%rbp)
    11c0:       c6 45 df 53             movb   $0x53,-0x21(%rbp)
    11c4:       c6 45 e0 5f             movb   $0x5f,-0x20(%rbp)
    11c8:       c6 45 e1 45             movb   $0x45,-0x1f(%rbp)
    11cc:       c6 45 e2 41             movb   $0x41,-0x1e(%rbp)
    11d0:       c6 45 e3 53             movb   $0x53,-0x1d(%rbp)
    11d4:       c6 45 e4 59             movb   $0x59,-0x1c(%rbp)
    11d8:       c6 45 e5 5f             movb   $0x5f,-0x1b(%rbp)
    11dc:       c6 45 e6 37             movb   $0x37,-0x1a(%rbp)
    11e0:       c6 45 e7 42             movb   $0x42,-0x19(%rbp)
    11e4:       c6 45 e8 43             movb   $0x43,-0x18(%rbp)
    11e8:       c6 45 e9 44             movb   $0x44,-0x17(%rbp)
    11ec:       c6 45 ea 39             movb   $0x39,-0x16(%rbp)
    11f0:       c6 45 eb 37             movb   $0x37,-0x15(%rbp)
    11f4:       c6 45 ec 31             movb   $0x31,-0x14(%rbp)
    11f8:       c6 45 ed 44             movb   $0x44,-0x13(%rbp)
    11fc:       c6 45 ee 7d             movb   $0x7d,-0x12(%rbp)
                                                                             
┌──(gio㉿kali)-[~/tercerparcial/asciiftw]
└─$ cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb | cut -d "$" -f2
0x70,-0x30(%rbp)
0x69,-0x2f(%rbp)
0x63,-0x2e(%rbp)
0x6f,-0x2d(%rbp)
0x43,-0x2c(%rbp)
0x54,-0x2b(%rbp)
0x46,-0x2a(%rbp)
0x7b,-0x29(%rbp)
0x41,-0x28(%rbp)
0x53,-0x27(%rbp)
0x43,-0x26(%rbp)
0x49,-0x25(%rbp)
0x49,-0x24(%rbp)
0x5f,-0x23(%rbp)
0x49,-0x22(%rbp)
0x53,-0x21(%rbp)
0x5f,-0x20(%rbp)
0x45,-0x1f(%rbp)
0x41,-0x1e(%rbp)
0x53,-0x1d(%rbp)
0x59,-0x1c(%rbp)
0x5f,-0x1b(%rbp)
0x37,-0x1a(%rbp)
0x42,-0x19(%rbp)
0x43,-0x18(%rbp)
0x44,-0x17(%rbp)
0x39,-0x16(%rbp)
0x37,-0x15(%rbp)
0x31,-0x14(%rbp)
0x44,-0x13(%rbp)
0x7d,-0x12(%rbp)
                                                                             
┌──(gio㉿kali)-[~/tercerparcial/asciiftw]
└─$ cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb | cut -d "$" -f2 | cut -d "," -f1
0x70
0x69
0x63
0x6f
0x43
0x54
0x46
0x7b
0x41
0x53
0x43
0x49
0x49
0x5f
0x49
0x53
0x5f
0x45
0x41
0x53
0x59
0x5f
0x37
0x42
0x43
0x44
0x39
0x37
0x31
0x44
0x7d
                                                                             
┌──(gio㉿kali)-[~/tercerparcial/asciiftw]
└─$ cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb | cut -d "$" -f2 | cut -d "," -f1 | tr -d "\n"
0x700x690x630x6f0x430x540x460x7b0x410x530x430x490x490x5f0x490x530x5f0x450x410x530x590x5f0x370x420x430x440x390x370x310x440x7d                                                                             
┌──(gio㉿kali)-[~/tercerparcial/asciiftw]
└─$ cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb | cut -d "$" -f2 | cut -d "," -f1 | tr -d "\n" | sed 's\0x\ 0x\g'
 0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x41 0x53 0x43 0x49 0x49 0x5f 0x49 0x53 0x5f 0x45 0x41 0x53 0x59 0x5f 0x37 0x42 0x43 0x44 0x39 0x37 0x31 0x44 0x7d                                                                             
┌──(gio㉿kali)-[~/tercerparcial/asciiftw]
└─$ cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb | cut -d "$" -f2 | cut -d "," -f1 | tr -d "\n" | sed 's\0x\ 0x\g' | sed 's\^ \\g'
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x41 0x53 0x43 0x49 0x49 0x5f 0x49 0x53 0x5f 0x45 0x41 0x53 0x59 0x5f 0x37 0x42 0x43 0x44 0x39 0x37 0x31 0x44 0x7d

┌──(gio㉿kali)-[~/tercerparcial/asciiftw]
└─$ cat disassembled_asciiftw.txt | grep "<main>:" -A 40 | grep movb | cut -d "$" -f2 | cut -d "," -f1 | tr -d "\n" | sed 's\0x\ 0x\g' | sed 's\^ \\g' | xxd -p -r
picoCTF{ASCII_IS_EASY_7BCD971D}       
```
# Notas adicionales
# Referencias
