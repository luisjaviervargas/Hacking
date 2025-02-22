## Descripción

I accidentally wrote the flag down. Good thing I deleted it! You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/137/challenge.zip)

## Solución

***
Para este ejercicio simplemente hay que seguir los pasos dados y utilizar lo aprendido del ejercicio de collaborative development. 

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF        
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c_titan/137/challenge.zip'
--2025-02-22 13:54:05--  https://artifacts.picoctf.net/c_titan/137/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 2600:9000:25ed:8200:16:5ec5:2840:93a1, 2600:9000:25ed:f800:16:5ec5:2840:93a1, 2600:9000:25ed:5400:16:5ec5:2840:93a1, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|2600:9000:25ed:8200:16:5ec5:2840:93a1|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19197 (19K) [application/octet-stream]
Saving to: ‘challenge.zip’

challenge.zip     100%[=============>]  18.75K  --.-KB/s    in 0.001s  

2025-02-22 13:54:05 (12.7 MB/s) - ‘challenge.zip’ saved [19197/19197]
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ unzip challenge.zip  

┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ cd drop-in 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ ls    
message.txt
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ cat message.txt 
TOP SECRET
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git reflog          
ef0b7cc (HEAD -> master) HEAD@{0}: commit: remove sensitive info
ea859bf HEAD@{1}: commit (initial): create flag
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git checkout ea859bf       
Note: switching to 'ea859bf'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c new-branch-name

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at ea859bf create flag
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ cat message.txt 
picoCTF{s@n1t1z3_cf09a485}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ 

Respuestas: picoCTF{s@n1t1z3_cf09a485}

***
## Notas Adicionales

## Referencias