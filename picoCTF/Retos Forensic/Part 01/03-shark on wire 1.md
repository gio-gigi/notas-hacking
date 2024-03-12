# Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
# Pistas
1. Try using a tool like Wireshark
# Solución
```
┌──(gio㉿kali)-[~/picoctf/forensic/sharkonwire1]
└─$ ls
capture.pcap
                                                                             
┌──(gio㉿kali)-[~/picoctf/forensic/sharkonwire1]
└─$ wireshark capture.pcap &
[1] 14363

picoCTF{StaT31355_636f6e6e}
```
![[Imagen de WhatsApp 2024-03-12 a las 12.39.53_f5cb5dc9 1.jpg]]
# Notas adicionales
pcap: Una captura de paquetes, se pueden guardar en paquetes apk. Se usa en el ambito de redes. Es un formato especifico de paquetes.
# Referencias
- Wirehark