## Descripción

How well can you perfom basic binary operations?

Additional details will be available after launching your challenge instance.
nc titan.picoctf.net 61061

## Solución

***
En este ejercicio solo se tiene que meter los datos que se piden para que se nos muestre la bandera.

┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ nc titan.picoctf.net 61061

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 01010100
Binary Number 2: 00100101


Question 1/6:
Operation 1: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 1111001
Incorrect. Try again
Enter the binary result: 01110101
Correct!

Question 2/6:
Operation 2: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 110000100100                        
Correct!

Question 3/6:
Operation 3: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00000100
Correct!

Question 4/6:
Operation 4: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 1111001
Correct!

Question 5/6:
Operation 5: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 00010010
Correct!

Question 6/6:
Operation 6: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 10101000
Correct!

Enter the results of the last operation in hexadecimal: A8

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_675602ae}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Resultado: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_675602ae}

***
## Notas Adicionales

## Referencias

https://www.rapidtables.com/calc/math/binary-calculator.html