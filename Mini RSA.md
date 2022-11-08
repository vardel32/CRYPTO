# Mini RSA
#picoCTF2019 #CRYPTO 
## Objetivo
Let's decrypt this: [ciphertext](https://jupiter.challenges.picoctf.org/static/d21037ad23ed84cfff20a84768a0f2b2/ciphertext)? Something seems a bit small.
	
## Solución
Si e es muy pequeña, ademas de que el mensaje cifrado es corto, entonces se puede ignorar a n para de este modo tener las siguientes formulas.
- c = m^e mod n
- c = n ^ 3
- m = 3 raíz c.
Primeramente hay que instalar una librería que permite hacer cálculos con números grandes sin perder precisión, así como la librería utilizada en retos anteriores para calcular el modulo inverso.

```bash
┌──(kali㉿kali)-[~/Downloads/CRYPTO/minirsa]
└─$ sudo python3 -m pip install gmpy2 
┌──(kali㉿kali)-[~/Downloads/CRYPTO/minirsa]
└─$ sudo python3 -m pip install pycryptodome
```

Posteriormente mediante python ejecutamos las siguientes lineas de código.

```python
┌──(kali㉿kali)-[~/Downloads/CRYPTO/minirsa]
└─$ python3       
Python 3.10.5 (main, Jun  8 2022, 09:26:22) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from gmpy2 import *
>>> from Crypto.Util.number import long_to_bytes 
>>> #Se establece la precision de calculo de la libreria gmpy2
>>> gmpy2.get_context().precision=2048
>>> #2048 bytes es la longitud de la llave
>>> e = 3
>>> c = 2205316413931134031074603746928247799030155221252519872650073010782049179856976080512716237308882294226369300412719995904064931819531456392957957122459640736424089744772221933500860936331459280832211445548332429338572369823704784625368933
>>> root, exact = iroot(c,e)
>>> print(long_to_bytes(root))
b'picoCTF{n33d_a_lArg3r_e_ccaa7776}'

```

Bandera:
==picoCTF{n33d_a_lArg3r_e_ccaa7776}==
## Notas adicionales
c - texto cifrado
m - mensaje texto plano
p - primo 1
q - primo 2
n - modulo
tn - totient n (euler)
e - exponente (llave publica) 2^16+1=65537
d - llave privada
n=p* q
tn = (p-1)* (q-1)
d = e mod inv tn     /     inverse(e,tn)
Encriptar : c = m^e mod n      /      pow (m,e,n)
Desencriptar: m = c^d mod n     /       pow(c,d,n)
## Referencias
