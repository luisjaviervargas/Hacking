
## Descripción

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm) has extraordinarily helpful information...
## Solución

***
Para este reto primero descargamos el archivo que da el reto, después con un cat vemos el contenido del archivo y con el comando file vemos que es un ejecutable, después de esto le otorgamos permisos para que pueda ejecutar el archivo y obtener la bandera. 

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ wget 'https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm'
--2025-02-19 12:44:20--  https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: ‘warm’

warm              100%[=============>]  10.68K  --.-KB/s    in 0s      

2025-02-19 12:44:21 (172 MB/s) - ‘warm’ saved [10936/10936]

                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ cat warm                                     
ELF>�@8"@8      @"!@@@�888

 XX/lib64/ld-linux-x86-64.so.2GNUGNU�]���n�Q�f����G4�Fj�K 
                                                          -&g v "libc.so.6putsprintf__cxa_finalizestrcmp__libc_start_mainGLIBC_2.2.5_ITM_deregis � � � � �� � � H�H�}_start___ITM_registerTMCloneTableu▒i       ?�
 H��t��H���5*
 �%,
 @�%*
 h������%"
 h������%▒
 h������%2
cH�=���� �DH�=��PTL��H�
 UH�
]��f.�]�@f.�H�=� H��t    H�5�    UH)�H��H��H��H��?H�H��t▒H��     H��t
                                                                     ]��f�]�@f.��=y      u/H�=W  UH��t
����H����Q       ]����fDUH��]�f���UH��H���}�H�u��}�uH�=�������KH�E�H�H�H�5�H���������uH�=��i����H�E�H�H�H��H�=:��X������DAWAVI��AUATL�%F UH�-F SA��I��L)�H�H�������H��t 1��L��L��D��A��H��H9�u�H�[]A\A]A^A_Ðf.���H�H��Hello user! Pass me a -h to learn what I can do!-hOh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}I don't know what '%s' means! I do know what -h means though!
<��������▒���X"�����������0zRx
                             ����+zRx
                                    $8���@F▒J
l                                            �?▒;*3$"DP��\R���qA�C
D|����eB�B▒�E �B(�H0�H8�M@r8A0A(B B▒B�������
���o���                                     `
�
 �� GCC: (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.0�q�
                                               �▒�q��x�zin���i��%��▒   ��b      k��     ���     d��▒    S��     ���(
��0
��8
�@
��H
@�P
m�X
R`
�
Xh
�
 bp
Vbt

px
�F�
rT�
I▒^�
�n�
%{�
�-��
�.��
�/��
�0��
�2-�
^3b�
b5t�
�X  �>▒���      ��R
▒         �n
8�/?��@��A��P�X��X��Xd▒b
                        ������q�9*b�9��%

                                        ;
                                         I$

                                           >
                                            $

                                             >
                                              



                                             I&I

                                               :
                                                ;
:
 ;
  I8

:
 ;I8

    :
     ;

!I/   I
   <4:
      ;I?<4:
            ;
             I?<!.?:
                    ;
                     '@▒�B:
8#TT 1tt$D���o�N           ;
i@��'��30t�@▒� ▒��▒V���^�*� >                                                                        pes.hlibio.hstdio.hsys_errlist.h   ��g�zɿ�_┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ file warm
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=985d9586d46e8651ab66c2fbb5a5473492466aa3, with debug_info, not stripped
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ ./warm                 
zsh: permission denied: ./warm
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ chmod +x warm                 
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ ./warm
Hello user! Pass me a -h to learn what I can do!
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}

***
## Notas Adicionales

## Referencias