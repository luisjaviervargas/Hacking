## Descripción

What was I last working on? I remember writing a note to help me remember... You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/162/challenge.zip)

## Solución

***
Para este ejercicio solo hay que descargar el el archivo que se necesita para resolver el reto, descomprimirlo y Despues poner el comando git log para poder ver la bandera necesaria.  

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF        
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c_titan/162/challenge.zip'
--2025-02-22 14:00:20--  https://artifacts.picoctf.net/c_titan/162/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 2600:9000:21ec:f600:16:5ec5:2840:93a1, 2600:9000:21ec:f000:16:5ec5:2840:93a1, 2600:9000:21ec:b600:16:5ec5:2840:93a1, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|2600:9000:21ec:f600:16:5ec5:2840:93a1|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17739 (17K) [application/octet-stream]
Saving to: ‘challenge.zip’

challenge.zip     100%[=============>]  17.32K  --.-KB/s    in 0.002s  

2025-02-22 14:00:20 (9.72 MB/s) - ‘challenge.zip’ saved [17739/17739]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ unzip challenge.zip 
Archive:  challenge.zip
   creating: drop-in/
  inflating: drop-in/message.txt     
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/master  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/43/
 extracting: drop-in/.git/objects/43/246218ab4fc7b30e9a9dff073e012316851469  
   creating: drop-in/.git/objects/25/
 extracting: drop-in/.git/objects/25/16effb8d70e33bdd0023629b164a77225e1ec2  
   creating: drop-in/.git/objects/71/
 extracting: drop-in/.git/objects/71/2314f105348e295f8cadd7d7dc4e9fa871e9a2  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/master  
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ cd drop-in           
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git log              
commit 712314f105348e295f8cadd7d7dc4e9fa871e9a2 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:26 2024 +0000

    picoCTF{t1m3m@ch1n3_e8c98b3a}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ 

Respuestas: picoCTF{t1m3m@ch1n3_e8c98b3a}

***
## Notas Adicionales

## Referencias