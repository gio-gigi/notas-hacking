# Objetivo
We have several pages hidden. Can you find the one with the flag?The website is running [here](http://saturn.picoctf.net:65455/).
# Pistas
1. folders folders folders
# Solución
1. Inspeccionar la pagina para encontrar las rutas:
	1. /secret/index
		```
		<link rel="stylesheet" href="hidden/file.css">	
		```
		2. /secret/hidden/index.html
		```
		<link href="superhidden/login.css" rel="stylesheet">
		```
		3. /secret/hidden/superhidden/index.html
		```
		# Finally. You found me. But can you see me

### picoCTF{succ3ss_@h3n1c@10n_39849bcf}
		```
# Notas adicionales
# Referencias