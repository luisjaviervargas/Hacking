## Descripción

Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses. Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools! You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/5/challenge.zip)

`ssh -p 49197 ctf-player@atlas.picoctf.net` Using the password `1ad5be0d`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!

## Solución

***
El archivo que nos proporcionaba el reto nos daba una idea de como se podría encontrar el numero que se necesitaba para resolver el reto, así que solo era intentarlo hasta lograrlo

┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ ssh -p 49197 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Permission denied, please try again.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 750
Lower! Try again.
Enter your guess: 600
Lower! Try again.
Enter your guess: 550
Lower! Try again.
Enter your guess: 525
Higher! Try again.
Enter your guess: 540
Lower! Try again.
Enter your guess: 530
Lower! Try again.
Enter your guess: 526
Higher! Try again.
Enter your guess: 528
Higher! Try again.
Enter your guess: 529
Congratulations! You guessed the correct number: 529
Here's your flag: picoCTF{g00d_gu355_3af33d18}
Connection to atlas.picoctf.net closed.
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{g00d_gu355_3af33d18}

***
## Notas Adicionales

## Referencias