# rsa-pop-quiz
#picoCTF2019 #CRYPTO 
## Objetivo
Class, take your seats! It's PRIME-time for a quiz... `nc jupiter.challenges.picoctf.org 58617`
## Solución

## Notas adicionales
RSA
p - número primo
q - número primo
n - modulo
tn - totient n t
e - exponente (llave publica)
d - llave 
c -  mensaje cifrado
m - mensaje en texto plano
- Primero se eligen dos números primos, p y q.
- Se calcula n = p * q
- tn = (p-1) * (q-1)
- d = e modulo inverso tn

Ecnriptar:
c = m ^ e  mod n
Desencriptar
m = c ^ d mod n
## Referencias
