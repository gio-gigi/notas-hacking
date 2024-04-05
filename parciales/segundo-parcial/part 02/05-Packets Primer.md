# Objetivo
Download the packet capture file and use packet analysis software to find the flag.

- [Download packet capture](https://artifacts.picoctf.net/c/194/network-dump.flag.pcap)
# Pistas
1. Wireshark, if you can install and use it, is probably the most beginner friendly packet analysis software product.
# Solución
```
┌──(gio㉿kali)-[~/picoctf/forensic/packetsprimer]
└─$ ls
network-dump.flag.pcap
                                                                                                      
┌──(gio㉿kali)-[~/picoctf/forensic/packetsprimer]
└─$ wireshark network-dump.flag.pcap
```
tcp.stream eq 0:
```
p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ c e c c a a 7 f }
```

# Notas adicionales
# Referencias