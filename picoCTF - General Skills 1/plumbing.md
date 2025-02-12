## Descripción

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 7480`.
## Solución

***
Para resolver el siguiente ejercicio utilice el comando nc para saber el contenido del link dado por el ejercicio y me di cuenta de que era un texto demasiado largo y entre todo ese texto debería de estar esa bandera, así que decidí meter todo el contenido en un archivo .txt para después utilizar el comando grep en el archivo y así encontrar la bandera.

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ nc jupiter.challenges.picoctf.org 7480 > CTF10.txt

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ grep picoCTF CTF10.txt                                
picoCTF{digital_plumb3r_06e9d954}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{digital_plumb3r_06e9d954}

***

## Notas Adicionales

## Referencias