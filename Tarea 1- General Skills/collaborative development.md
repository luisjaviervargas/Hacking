## Descripción

My team has been working very hard on new features for our flag printing program! I wonder how they'll work together? You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/69/challenge.zip)

## Solución

***
Para este ejercicio se tenia que trabajar con el comando git para poder obtener la bandera, siguiendo los pasos que daba cada parte del programa. 

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF/drop-in 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ cat flag.py                  
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git log                    
commit ad37f59bfdcb1e8052bf7e12e1d89a2adb315cf9 (HEAD -> feature/part-1, main)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:38 2024 +0000

    add part 1

commit eb4de2a9826332633c62e44a1a130d9b1a88171a
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:38 2024 +0000

    init flag printer
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git show
commit ad37f59bfdcb1e8052bf7e12e1d89a2adb315cf9 (HEAD -> feature/part-1, main)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:38 2024 +0000

    add part 1

diff --git a/flag.py b/flag.py
index 77d6cec..6e17fb3 100644
--- a/flag.py
+++ b/flag.py
@@ -1 +1,2 @@
 print("Printing the flag...")
+print("picoCTF{t3@mw0rk_", end='')
\ No newline at end of file
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ ls -la
total 16
drwxr-xr-x 3 kali kali 4096 Feb 22 13:23 .
drwxrwxr-x 4 kali kali 4096 Feb 22 13:21 ..
-rw-rw-r-- 1 kali kali   64 Feb 22 13:23 flag.py
drwxr-xr-x 8 kali kali 4096 Feb 22 13:29 .git
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ reconect 
reconect: command not found
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git merge feature/part-2     
Committer identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'kali@kali.(none)')
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git config --global user.email "you@example.com"
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git config --global user.name "Your Name"

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git merge feature/part-2                        
Auto-merging flag.py
CONFLICT (content): Merge conflict in flag.py
Automatic merge failed; fix conflicts and then commit the result.
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ cat flag.py 
print("Printing the flag...")
<<<<<<< HEAD
print("picoCTF{t3@mw0rk_", end='')
=======

print("m@k3s_th3_dr3@m_", end='')
>>>>>>> feature/part-2
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git add flag.py         
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git commit -m mergeg                     
[feature/part-1 b0a4f42] mergeg
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ cat flag.py 
print("Printing the flag...")
<<<<<<< HEAD
print("picoCTF{t3@mw0rk_", end='')
=======

print("m@k3s_th3_dr3@m_", end='')
>>>>>>> feature/part-2
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git merge feature/part-3                 
Auto-merging flag.py
CONFLICT (content): Merge conflict in flag.py
Automatic merge failed; fix conflicts and then commit the result.
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git add flag.py         
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ git commit -m metged    
[feature/part-1 46c04d0] metged
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ cat flag.py 
print("Printing the flag...")
<<<<<<< HEAD
<<<<<<< HEAD
print("picoCTF{t3@mw0rk_", end='')
=======

print("m@k3s_th3_dr3@m_", end='')
>>>>>>> feature/part-2
=======

print("w0rk_e4b79efb}")
>>>>>>> feature/part-3
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF/drop-in]
└─$ 

Respuesta: picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_e4b79efb}

***
## Notas Adicionales

## Referencias

https://www.youtube.com/watch?v=_CH5IQewkzw&ab_channel=AnonymousWorld