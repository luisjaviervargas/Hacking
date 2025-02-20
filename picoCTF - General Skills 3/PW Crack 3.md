## Descripción

Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución

***
Para este ejercicio se tenia que buscar la manera de encontrar la contraseña correcta que nos deje  ver la bandera, para ello mediante un for se tenia que intentar con cada una de las 7 opciones para saber cual es la contraseña correcta y así poder encontrar la bandera. 

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/17/level3.py'
--2025-02-20 11:59:03--  https://artifacts.picoctf.net/c/17/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.61, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: ‘level3.py’

level3.py         100%[=============>]   1.31K  --.-KB/s    in 0s      

2025-02-20 11:59:04 (12.5 MB/s) - ‘level3.py’ saved [1337/1337]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/17/level3.flag.txt.enc'
--2025-02-20 11:59:12--  https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.26, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: ‘level3.flag.txt.enc’

level3.flag.txt.e 100%[=============>]      31  --.-KB/s    in 0s      

2025-02-20 11:59:12 (15.0 MB/s) - ‘level3.flag.txt.enc’ saved [31/31]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/17/level3.hash.bin'     
--2025-02-20 11:59:36--  https://artifacts.picoctf.net/c/17/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.64, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: ‘level3.hash.bin’

level3.hash.bin   100%[=============>]      16  --.-KB/s    in 0s      

2025-02-20 11:59:37 (22.1 MB/s) - ‘level3.hash.bin’ saved [16/16]
																		
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ python3 level3.py
That password is incorrect
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ python3 level3.py
That password is incorrect
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ python3 level3.py
That password is incorrect
That password is incorrect
Welcome back... your flag, user:
87ab
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{m45h_fl1ng1ng_cd6ed2eb}

***
## Notas Adicionales

## Referencias

https://www.youtube.com/watch?v=Dn4NruKchkw&ab_channel=AlmondForce