# Objetivo
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 49039`, but it doesn't speak English...
# Pistas
1. You can practice using netcat with this picoGym problem: [what's a netcat?](https://play.picoctf.org/practice/challenge/34)
2. You can practice reading and writing ASCII with this picoGym problem: [Let's Warm Up](https://play.picoctf.org/practice/challenge/22)
# Solución
```
giogi-picoctf@webshell:~$ nc mercury.picoctf.net 49039
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
51 
100 
56 
52 
101 
100 
99 
56 
125 
10 
```
![[Pasted image 20240227124445.png]]
# Notas adicionales
# Referencias
- https://www.prepostseo.com/tool/decimal-to-ascii