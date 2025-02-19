
## Descripción

Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/503/big-zip-files.zip)
## Solución

***
Primero se descarga el archivo zip en la computadora, para después descomprimir el zip y poder utilizar el comando grep para poder leer todos los archivo en busca de la palabra clave picoCTF

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/503/big-zip-files.zip'
--2025-02-19 11:09:13--  https://artifacts.picoctf.net/c/503/big-zip-files.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.26, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3182988 (3.0M) [application/octet-stream]
Saving to: ‘big-zip-files.zip’

big-zip-files.zip 100%[=============>]   3.04M  6.80MB/s    in 0.4s    

2025-02-19 11:09:15 (6.80 MB/s) - ‘big-zip-files.zip’ saved [3182988/3182988]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ unzip big-zip-files.zip
Archive:  big-zip-files.zip
   creating: big-zip-files/
 extracting: big-zip-files/jpvaawkrpno.txt  
  inflating: big-zip-files/oxbcyjsy.txt  
  inflating: big-zip-files/hllhxlvvdgiii.txt 

──(kali㉿kali)-[~/Documents/retosCTF]
└─$ grep -r "picoCTF" big-zip-files
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{gr3p_15_m4g1c_ef8790dc}
***
## Notas Adicionales

## Referencias