# la cifra de
#picoCTF2019 #CRYPTO 
## Objetivo
I found this cipher in an old book. Can you figure out what it says? Connect with `nc jupiter.challenges.picoctf.org 32411`.
## Solución
Devuelve un texto cifrado, tras intentar hacer rot 13, base64, base octal se llega a la conclusion de que se utiliza el cigrado Vigenere, sin embargo no poseemos la clave para descifrarlo, entonces utilizando una página que permite crackear el código obtenemos la bandera.
Bandera cifrada:
==hgqqpohzCZK{m311a50_0x_a1rn3x3_h1ah3x7g996649}==
Bandera descifrada:
==picoCTF{b311a50_0r_v1gn3r3_c1ph3r7b996649}==

## Notas adicionales

## Referencias
https://www.guballa.de/vigenere-solver
