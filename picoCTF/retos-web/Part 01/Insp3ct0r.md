# Objetivo
Kishor Balan tipped us off that the following code may need inspection: `https://jupiter.challenges.picoctf.org/problem/41511/` ([link](https://jupiter.challenges.picoctf.org/problem/41511/)) or http://jupiter.challenges.picoctf.org:41511
# Pistas
1. How do you inspect web code on a browser?
2. There's 3 parts.
# Solución
```
|<!doctype html>|
||<html>|
||<head>|
||<title>My First Website :)</title>|
||<link href="[https://fonts.googleapis.com/css?family=Open+Sans\|Roboto](https://fonts.googleapis.com/css?family=Open+Sans\|Roboto)" rel="stylesheet">|
||<link rel="stylesheet" type="text/css" href="[mycss.css](https://jupiter.challenges.picoctf.org/problem/41511/mycss.css)">|
||<script type="application/javascript" src="[myjs.js](https://jupiter.challenges.picoctf.org/problem/41511/myjs.js)"></script>|
||</head>|
|||
||<body>|
||<div class="container">|
||<header>|
||<h1>Inspect Me</h1>|
||</header>|
|||
||<button class="tablink" onclick="openTab('tabintro', this, '#222')" id="defaultOpen">What</button>|
||<button class="tablink" onclick="openTab('tababout', this, '#222')">How</button>|
|||
||<div id="tabintro" class="tabcontent">|
||<h3>What</h3>|
||<p>I made a website</p>|
||</div>|
|||
||<div id="tababout" class="tabcontent">|
||<h3>How</h3>|
||<p>I used these to make this site: <br/>|
||HTML <br/>|
||CSS <br/>|
||JS (JavaScript)|
||</p>|
||<!-- Html is neat. Anyways have 1/3 of the flag: picoCTF{tru3_d3 -->|
||</div>|
|||
||</div>|
|||
||</body>|
||</html>|
||

#tabintro { background-color: #ccc; }
#tababout { background-color: #ccc; }

/* You need CSS to make pretty pages. Here's part 2/3 of the flag: t3ct1ve_0r_ju5t */

window.onload = function() {
    openTab('tabintro', this, '#222');
}

/* Javascript sure is neat. Anyways part 3/3 of the flag: _lucky?832b0699} */
```
# Notas adicionales
- Podemos ver el código fuente dando clic derecho.
# Referencias
- https://jupiter.challenges.picoctf.org/problem/41511/