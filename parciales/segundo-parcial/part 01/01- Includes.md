# Objetivo
Can you get the flag?Go to this [website](http://saturn.picoctf.net:50761/) and see what you can discover.
# Pistas
1. Is there more code than what the inspector initially shows?
# Solución
1. El sitio web, muestra una alerta.
2. Ir directo al codigo fuente, styles.css.
```
body {
  background-color: lightblue;
}

/*  picoCTF{1nclu51v17y_1of2_  */
```
3. Abrimos el script de javascript "[script.js].
```
function greetings()
{
  alert("This code is in a separate file!");
}

//  f7w_2of2_df589022}
```
picoCTF{1nclu51v17y_1of2_f7w_2of2_df589022}
# Notas adicionales
# Referencias