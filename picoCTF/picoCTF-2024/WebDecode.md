## Objetivo
Do you know how to use the web inspector?Start searching [here](http://titan.picoctf.net:53646/) to find the flag
## Pistas
1.-Use the web inspector on other files included by the web page.
2.-The flag may or may not be encoded
## Solución
La bandera se encuentra en la pagina de About, donde al ver el código fuente podebemos observar una clase que esta ne base 64
```
|   |
|---|
|<section class="about" notify_true="cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfMjgzZTYyZmV9">|
||<h1>|
||Try inspecting the page!! You might find it there|
||</h1>|
||<!-- .about-container -->|
||</section>|
||<!-- .about -->|
||<section class="why">|
||<footer>|
||<div class="bottombar">|
||Copyright © 2023 Your_Name. All rights reserved.|
||</div>|
```
Al momento de decodificarla obtendremos la contraseña
picoCTF{web_succ3ssfully_d3c0ded_283e62fe}
## Notas Adicionales
## Referencias
https://www.base64decode.org