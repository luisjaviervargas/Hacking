## Descripción

Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell. [Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
## Solución

***
   Para este ejercicio simplemente se tenia que descargar el ejecutable de python y correrlo para obtener la bandera. 
   
   ┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/34/runme.py'
--2025-02-20 11:50:11--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.28, 13.225.222.120, 13.225.222.105, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.28|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: ‘runme.py’

runme.py          100%[=============>]     270  --.-KB/s    in 0s      

2025-02-20 11:50:12 (531 MB/s) - ‘runme.py’ saved [270/270]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ python3 runme.py 
picoCTF{run_s4n1ty_run}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{run_s4n1ty_run}
***
## Notas Adicionales

## Referencias