# Objetivo
Oracles can be your best friend, they will decrypt anything, except the flag's ciphertext. How will you break it? Connect with `nc mercury.picoctf.net 10333`.
# Pistas
1. What can you do with a different pair of ciphertext and plaintext? What if it is not so different after all...

# Solución
```
 >>> n =156135826956841705506907490004789510483548284453015054948509641200938318578403483662083160108823331855170527268744432337715328759715153297182805080289840611718870648028518600609611855551460658622754437319586406455462207739887987405201732376335142591856895562250256748206084934558331998707474617393344684698429
>>> e = 65537
>>> c = 111416041126780603217628203803317135242903077741462723564855592297066562407631747585985713322718939200379957082084311790113492624456751850243612113967162692866447341191042997636982998784643788070612849973506924994189738615359555771227641335750651616862902068271769405728780939993803951557599519003107392743175
>>> x = pow(2, e, n)
>>> c * x
5698218990214187472437227544756014240243214437598709610065152834604141269785400429910735570249720412068879482409640068970149601937867131934291874650460074490782156112411503763896080377826941567336849680459399109790756150391958003501498736059886016600478882486934142010436508906360799337974387144279263069830825250604730252267126288707271504774200908330548651173253192844468719381450613221287112379644901495713027431848908668690038610350071046423056336870250556231354556867895708287593923845512345983061481503377424540155592724237836087388100665930595677124924882414824523609313874946634994240709693358986034273870100 
>>> m = 580550060391700078946913236734911770139931497702556153513487440893406629034802718534645538074938502890768853279675297196794 //2
>>> bytearray.fromhex(format(m, 'x')).decode()
'picoCTF{m4yb3_Th0se_m3s54g3s_4r3_difurrent_1772735}'

```

```
picoCTF{m4yb3_Th0se_m3s54g3s_4r3_difurrent_1772735}
```
# Notas adicionales
# Referencias