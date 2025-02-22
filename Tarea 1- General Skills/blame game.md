## Descripción

Someone's commits seems to be preventing the program from working. Who is it? You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/156/challenge.zip)

## Solución

***
Para este ejercicio se tenia que descargar el archivo proporcionado por el reto, para después descomprimirlo, luego nos posicionamos mediante el comando cd en el archivo que nos dio al descomprimirlo y mediante el comando git ejecutamos el mensaje del archivo python para obtener la bandera. 

┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c_titan/156/challenge.zip'
--2025-02-22 13:05:47--  https://artifacts.picoctf.net/c_titan/156/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 2600:9000:21ec:a800:16:5ec5:2840:93a1, 2600:9000:21ec:4c00:16:5ec5:2840:93a1, 2600:9000:21ec:8a00:16:5ec5:2840:93a1, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|2600:9000:21ec:a800:16:5ec5:2840:93a1|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 293739 (287K) [application/octet-stream]
Saving to: ‘challenge.zip.1’

challenge.zip.1   100%[=============>] 286.85K   890KB/s    in 0.3s    

2025-02-22 13:05:48 (890 KB/s) - ‘challenge.zip.1’ saved [293739/293739]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ unzip challenge1.zip 
																		
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ ls
Addadshashanammu      enc_flag             level3.flag.txt.enc
Addadshashanammu.zip  file                 level3.hash.bin
big-zip-files         files                level3.py
big-zip-files.zip     files.zip            ltdis.sh
challenge1.zip        fixme1.py            runme.py
challenge.zip         fixme2.py            serpentine.py
codebook.txt          flag                 -s.ltdis.x86_64.txt
code.py               home                 static
convertme.py          level1.flag.txt.enc  static.ltdis.strings.txt
convertme.py.1        level1.py            static.ltdis.x86_64.txt
CTF10.txt             level2.flag.txt.enc  strings
drop-in               level2.py            warm
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ cd drop-in           
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ ls
message.py
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git log message.py
commit 0351e0474493168ca76441c24630c17554fd09ca
Author: picoCTF{@sk_th3_1nt3rn_d2d29f22} <ops@picoctf.com>
Date:   Tue Mar 12 00:07:01 2024 +0000

    optimize file size of prod code

commit c9e851509190f5887e91339ee18087e3e77ebfda
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:01 2024 +0000

    create top secret project
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ 

***
## Notas Adicionales

## Referencias