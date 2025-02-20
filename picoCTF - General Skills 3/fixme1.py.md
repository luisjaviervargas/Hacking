## Descripción

Fix the syntax error in this Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/27/fixme1.py)

## Solución

***
En este ejercicio teníamos que arreglar el problema en el codigo para poder obtener la bandera, en este caso el error estaba en la ultima linea a causa de la sangria que tenia el print, mediante el comando nano se elimina esta sangria y se obtiene la bandera. 

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/27/fixme1.py'
--2025-02-20 11:10:45--  https://artifacts.picoctf.net/c/27/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.61, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: ‘fixme1.py’

fixme1.py         100%[=============>]     837  --.-KB/s    in 0s      

2025-02-20 11:10:45 (18.4 MB/s) - ‘fixme1.py’ saved [837/837]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ nano fixme1.py                         
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ python3 fixme1.py   
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{1nd3nt1ty_cr1515_182342f7}
***
## Notas Adicionales

## Referencias