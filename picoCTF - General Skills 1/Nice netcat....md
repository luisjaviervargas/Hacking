## Descripción

There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 7449`, but it doesn't speak English...
## Solución

***
Me metí a la pagina de CyberChef para resolver este ejercicio, y pase los números que me dio el comando dado por el ejercicio a decimal para poder obtener la bandera:

┌──(kali㉿kali)-[~]
└─$ nc mercury.picoctf.net 7449 
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
102 
50 
100 
55 
99 
97 
102 
97 
125 
10 
                                                                        
┌──(kali㉿kali)-[~]
└─$  

Respuesta: picoCTF{g00d_k1tty!_n1c3_k1tty!_f2d7cafa}

***

## Notas Adicionales

## Referencias

https://gchq.github.io/CyberChef/