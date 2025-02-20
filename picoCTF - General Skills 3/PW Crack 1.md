## Descripción

Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.
## Solución

***
Descargamos el programa y el archivo encriptado en el mismo directorio y Despues de ello vemos el contenido del programa para ver la contraseña de acceso, después corremos el programa, ponemos la contraseña  y así obtenemos la bandera.

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/12/level1.py'
--2025-02-20 11:35:28--  https://artifacts.picoctf.net/c/12/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.105, 13.225.222.120, 13.225.222.125, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.105|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: ‘level1.py’

level1.py         100%[=============>]     876  --.-KB/s    in 0.001s  

2025-02-20 11:35:28 (1.05 MB/s) - ‘level1.py’ saved [876/876]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/12/level1.flag.txt.enc'
--2025-02-20 11:35:41--  https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.28, 13.225.222.105, 13.225.222.120, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.28|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: ‘level1.flag.txt.enc’

level1.flag.txt.e 100%[=============>]      30  --.-KB/s    in 0s      

2025-02-20 11:35:41 (14.0 MB/s) - ‘level1.flag.txt.enc’ saved [30/30]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ cat level1.py 
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################


flag_enc = open('level1.flag.txt.enc', 'rb').read()



def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "8713"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_1_pw_check()
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ python3 level1.py
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{545h_r1ng1ng_1b2fd683}

***
## Notas Adicionales

## Referencias