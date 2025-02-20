## Descripción

Run the Python script and convert the given number from decimal to binary to get the flag. [Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)
## Solución

***
En este ejercicio simplemente teníamos que convertir el numero dado por el programa a binario para obtener la bandera. 

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/24/convertme.py'
--2025-02-20 11:02:46--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.120, 13.225.222.28, 13.225.222.105, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.120|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: ‘convertme.py.1’

convertme.py.1    100%[=============>]   1.16K  --.-KB/s    in 0s      

2025-02-20 11:02:46 (35.9 MB/s) - ‘convertme.py.1’ saved [1189/1189]
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ python3 convertme.py
If 53 is in decimal base, what is it in binary base?
Answer: 110101        
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{4ll_y0ur_b4535_722f6b39}

***
## Notas Adicionales

## Referencias