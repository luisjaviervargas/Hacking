## Descripción

Our flag printing service has started glitching! Additional details will be available after launching your challenge instance.

Our flag printing service has started glitching! `$ nc saturn.picoctf.net 58968`
## Solución

***
Ponemos en la terminal el codigo que se nos da para después convertir la bandera dada en terminal a la bandera final que necesitamos. 

┌──(kali㉿kali)-[~]
└─$ nc saturn.picoctf.net 58968
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
                                                                        
┌──(kali㉿kali)-[~]
└─$ 

Despues convertimos la bandera mediante la pagina de CyberChef  con ASCCI para obtener la bandera que seria la siguiente:

Respuesta: picoCTF{gl17ch_m3_n07_9c42a45d}

***

## Notas Adicionales

## Referencias

https://gchq.github.io/CyberChef/