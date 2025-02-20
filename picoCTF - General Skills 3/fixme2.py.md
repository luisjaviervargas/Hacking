## Descripción

Fix the syntax error in the Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)

## Solución

***
Para solucionar el siguiente ejercicio se hizo lo mismo que en el ejercicio de fixme1. se descargo el archivo y mediante la opción nano inspeccionamos el contenido del programa y lo revisamos cuidadosamente para solucionar el error, que en este caso era en el ultimo if del programa, ya que el if solo tenia un = que causaba error ya que debía ser un doble igual ara comparar. 

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/6/fixme2.py'
--2025-02-20 11:18:40--  https://artifacts.picoctf.net/c/6/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.105, 13.225.222.28, 13.225.222.120, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.105|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: ‘fixme2.py’

fixme2.py         100%[=============>]   1.00K  --.-KB/s    in 0s      

2025-02-20 11:18:40 (11.3 MB/s) - ‘fixme2.py’ saved [1029/1029]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ nano fixme2.py 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
***
## Notas Adicionales

## Referencias