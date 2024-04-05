# Objetivo
The developer of this website mistakenly left an important artifact in the website source, can you find it?The website is [here](http://saturn.picoctf.net:63978/)
# Pistas
1. How could you mirror the website on your local machine so you could use more powerful tools for searching?
# Solución
1. La bandera se encuentra en los style.css del sitio.
```
 .navbar-expand-md .navbar-nav .nav-link {
     padding: 15px 48px;
     font-size: 16px;
     color: #000;
     line-height: 18px;
}
/** banner_main picoCTF{1nsp3ti0n_0f_w3bpag3s_ec95fa49} **/
 .carousel-indicators li {
     width: 20px;
     height: 20px;
     border-radius: 11px;
     background-color: #070000;
}
```
# Notas adicionales
# Referencias