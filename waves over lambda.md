# waves over lambda
#picoCTF2019 #CRYPTO 
## Objetivo
We made a lot of substitutions to encrypt this. Can you decrypt it? Connect with `nc jupiter.challenges.picoctf.org 43522`.
## Solución
Nos encontramos con un texto cifrado mediante substitución
```bash
┌──(kali㉿kali)-[~]
└─$ nc jupiter.challenges.picoctf.org 43522
-------------------------------------------------------------------------------
zxmbruvc fsrs wc oxlr jkub - jrshlsmzo_wc_z_xdsr_kupteu_xbjpulmruj
-------------------------------------------------------------------------------
fudwmb fue cxps vwps uv po ewcgxcuk qfsm wm kxmexm, w fue dwcwvse vfs trwvwcf plcslp, ume pues csurzf upxmb vfs txxyc ume pugc wm vfs kwtruro rsburewmb vrumcokdumwu; wv fue cvrlzy ps vfuv cxps jxrsymxqksebs xj vfs zxlmvro zxlke fureko juwk vx fuds cxps wpgxrvumzs wm esukwmb qwvf u mxtkspum xj vfuv zxlmvro. w jwme vfuv vfs ewcvrwzv fs mupse wc wm vfs snvrsps sucv xj vfs zxlmvro, alcv xm vfs txresrc xj vfrss cvuvsc, vrumcokdumwu, pxkeudwu ume tlyxdwmu, wm vfs pwecv xj vfs zurguvfwum pxlmvuwmc; xms xj vfs qwkescv ume ksucv ymxqm gxrvwxmc xj slrxgs. w quc mxv utks vx kwbfv xm umo pug xr qxry bwdwmb vfs snuzv kxzukwvo xj vfs zucvks eruzlku, uc vfsrs urs mx pugc xj vfwc zxlmvro uc osv vx zxpgurs qwvf xlr xqm xremumzs clrdso pugc; tlv w jxlme vfuv twcvrwvi, vfs gxcv vxqm mupse to zxlmv eruzlku, wc u juwrko qskk-ymxqm gkuzs. w cfukk smvsr fsrs cxps xj po mxvsc, uc vfso puo rsjrscf po pspxro qfsm w vuky xdsr po vrudskc qwvf pwmu.

```

Acudimos a una página de internet para poder romper l cifrado y obtener la clave utilizada para cifrar y obtenemos la siguiente información.
La llave utilizada para cifrar el texto es:
`utzesjbfwaykpmxghrcvldqnoi`
y la bandera es:
==frequency_is_c_over_lambda_ogfmaunraf==
## Notas adicionales

## Referencias
