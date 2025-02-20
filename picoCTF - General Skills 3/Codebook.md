## Descripción

Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/2/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/2/codebook.txt)
## Solución

***
Primero descargamos los dos archivos en el mismo directorio y corremos el programa de python para que nos de la bandera. 

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/2/code.py'
--2025-02-20 10:56:22--  https://artifacts.picoctf.net/c/2/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.125, 13.225.222.120, 13.225.222.105, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.125|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: ‘code.py’

code.py           100%[=============>]   1.25K  --.-KB/s    in 0s      

2025-02-20 10:56:23 (69.7 MB/s) - ‘code.py’ saved [1278/1278]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/2/codebook.txt'
--2025-02-20 10:56:31--  https://artifacts.picoctf.net/c/2/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.28, 13.225.222.125, 13.225.222.120, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.28|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: ‘codebook.txt’

codebook.txt      100%[=============>]      27  --.-KB/s    in 0s      

2025-02-20 10:56:32 (68.8 MB/s) - ‘codebook.txt’ saved [27/27]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ ls
Addadshashanammu      enc_flag             static
Addadshashanammu.zip  file                 static.ltdis.strings.txt
big-zip-files         files                static.ltdis.x86_64.txt
big-zip-files.zip     files.zip            strings
codebook.txt          flag                 warm
code.py               ltdis.sh
CTF10.txt             -s.ltdis.x86_64.txt
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ python3 code.py
picoCTF{c0d3b00k_455157_7d102d7a}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{c0d3b00k_455157_7d102d7a}
***
## Notas Adicionales

## Referencias