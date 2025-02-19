
## Descripción

To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 15130`.
## Solución

***
En este ejercicio solamente teníamos que convertir de el tipo de encriptado a la frase que significado, pero esto se puede hacer fácil gracias a herramientas que ya existen en internet, en mi caso use CyberChef para resolverlo.  

┌──(kali㉿kali)-[~]
└─$ nc jupiter.challenges.picoctf.org 15130

Let us see how data is stored
computer
Please give the 01100011 01101111 01101101 01110000 01110101 01110100 01100101 01110010 as a word.
...
you have 45 seconds.....

Input:
computer
Please give me the  155 141 160 as a word.
Input:
map
Please give me the 7375626d6172696e65 as a word.
Input:
submarine
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_02167de8}
                                                                        
┌──(kali㉿kali)-[~]
└─$ 

Respuesta: picoCTF{learning_about_converting_values_02167de8}

***
## Notas Adicionales

## Referencias

https://gchq.github.io/CyberChef/