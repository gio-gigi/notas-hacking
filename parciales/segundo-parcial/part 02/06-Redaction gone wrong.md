# Objetivo
Now you DON’T see me.This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?
# Pistas
1. How can you be sure of the redaction?
# Solución
```
┌──(gio㉿kali)-[~/picoctf/forensic/redationgonewrong]
└─$ open Financial_Report_for_ABC_Labs.pdf

```
Seleccionamos el texto incluyendo las lineas negras que tiene el pdf, mostrando las palabras ocultas:
```
Breakdown - Just painted over in MS word.
Cost Benefit Analysis
Credit Debit
This is not the flag, keep looking
Expenses from the
picoCTF{C4n_Y0u_S33_m3_fully}
```
# Notas adicionales
# Referencias