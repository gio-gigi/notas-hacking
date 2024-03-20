# Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.
# Pistas
# Solución
1. Usar wireshark.
```
┌──(gio㉿kali)-[~/picoctf/forensic/sharkonwire2]
└─$ wireshark capture.pcap
```
3. Crear un script de python usando scapy.
```
┌──(gio㉿kali)-[~/picoctf/forensic/sharkonwire2]
└─$ nano exp.py
 Código del script:
 from scapy.all import  *
packets = rdpcap('capture.pcap')

flag = ''
for p in packets:
        if UDP in p and p[UDP].dport == 22:
                if p[UDP].sport > 5000:
                        flag +=chr(p[UDP].sport - 5000)
```
5. Executar script
```
┌──(gio㉿kali)-[~/picoctf/forensic/sharkonwire2]
└─$ python3 exp.py
picoCTF{p1LLf3r3d_data_v1a_st3g0}
```
# Notas adicionales
- scapy: Modulo de manipulación de paquetes que es capaz de crear o decodificar paquetes, es capaz de mandar trafico de red, capturar paquetes de los protocolos.
# Referencias
