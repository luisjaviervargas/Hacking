## Descripción

Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
## Solución

***
Para este ejercicio se descargo el archivo ejecutable de python junto con el encriptado en el mismo directorio. después de esto checamos el codigo del ejecutable y se puede ver que la contraseña esta encriptada, así que simplemente hacemos un print de la contraseña para ver cual sera y la ponemos para obtener la bandera.  

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/14/level2.py'
--2025-02-20 11:40:50--  https://artifacts.picoctf.net/c/14/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.28, 13.225.222.120, 13.225.222.105, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.28|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: ‘level2.py’

level2.py         100%[=============>]     914  --.-KB/s    in 0s      

2025-02-20 11:40:51 (31.6 MB/s) - ‘level2.py’ saved [914/914]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/14/level2.flag.txt.enc'
--2025-02-20 11:41:07--  https://artifacts.picoctf.net/c/14/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.125, 13.225.222.28, 13.225.222.120, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.125|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: ‘level2.flag.txt.enc’

level2.flag.txt.e 100%[=============>]      31  --.-KB/s    in 0s      

2025-02-20 11:41:07 (72.1 MB/s) - ‘level2.flag.txt.enc’ saved [31/31]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ python3 level2.py 
4ec9
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{tr45h_51ng1ng_9701e681}

***
## Notas Adicionales

## Referencias