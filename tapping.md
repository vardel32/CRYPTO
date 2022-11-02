# tapping
#picoCTF2019 #CRYPTO 
## Objetivo
Theres tapping coming in from the wires. What's it saying `nc jupiter.challenges.picoctf.org 21610`.
## Solución
Al conectarse mediante netcat al puerto indicado por el reto el resultado es el siguiente...
```bash
┌──(kali㉿kali)-[~]
└─$ nc jupiter.challenges.picoctf.org 21610
.--. .. -.-. --- -.-. - ..-. { -- ----- .-. ... ...-- -.-. ----- -.. ...-- .---- ... ..-. ..- -. ...-- ----. ----- ..--- ----- .---- ----. ..... .---- ----. } 
                 
```

Es más que evidente que se trata de código morse.
Utilizando una página web que permite traducir de código morse a ASCII obtenemos lo siguiente:
picoctf{m0rs3c0d31sfun3902019519}
## Notas adicionales

## Referencias
http://www.unit-conversion.info/texttools/morse-code/