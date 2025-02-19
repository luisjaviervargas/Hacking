
## Descripción

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?
## Solución

***
En este solamente se tenia que utilizar el comando string para obtener la cadena que coincidiera con picoCTF.

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF                        
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings'
--2025-02-19 12:30:53--  https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: ‘strings’

strings           100%[=============>] 757.84K  2.15MB/s    in 0.3s    

2025-02-19 12:30:54 (2.15 MB/s) - ‘strings’ saved [776032/776032]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ strings strings | grep picoCTF
picoCTF{5tRIng5_1T_7f766a23}

Respuesta:  picoCTF{5tRIng5_1T_7f766a23}

***
## Notas Adicionales

## Referencias