## Descripción

Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/35/serpentine.py)
## Solución

***
Para este ejercicio solo se tenia que checar el codigo y buscar la función para mostrar la bandera y mostrarla primero para así obtener la bandera. 

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://artifacts.picoctf.net/c/35/serpentine.py'
--2025-02-20 12:23:20--  https://artifacts.picoctf.net/c/35/serpentine.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.28, 13.225.222.120, 13.225.222.105, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.28|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2550 (2.5K) [application/octet-stream]
Saving to: ‘serpentine.py’

serpentine.py     100%[=============>]   2.49K  --.-KB/s    in 0s      

2025-02-20 12:23:21 (243 MB/s) - ‘serpentine.py’ saved [2550/2550]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ python3 serpentine.py 
/home/kali/Documents/retosCTF/serpentine.py:38: SyntaxWarning: invalid escape sequence '\ '
  '''

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) a

-----------------------------------------------------
Keep it up!
-----------------------------------------------------


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b

Oops! I must have misplaced the print_flag function! Check my source code!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) c
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ python3 serpentine.py
/home/kali/Documents/retosCTF/serpentine.py:38: SyntaxWarning: invalid escape sequence '\ '
  '''
picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}

***
## Notas Adicionales

## Referencias