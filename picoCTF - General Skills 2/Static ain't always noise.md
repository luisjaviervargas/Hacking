
## Descripción

Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/static)? This [BASH script](https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/ltdis.sh) might help!
## Solución

***

┌──(kali㉿kali)-[~]
└─$ cd Documents/retosCTF                                             
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ cat ltdis.sh   
#!/bin/bash
#!/bin/bash


echo "Attempting disassembly of $1 ..."


#This usage of "objdump" disassembles all (-D) of the first file given by 
#invoker, but only prints out the ".text" section (-j .text) (only section
#that matters in almost any compiled program...

objdump -Dj .text $1 > $1.ltdis.x86_64.txt


#Checkthat $1.ltdis.x86_64.txt is non-empty
#Continue if it is, otherwise print error and eject

if [ -s "$1.ltdis.x86_64.txt" ]
then
        echo "Disassembly successful! Available at: $1.ltdis.x86_64.txt"

        echo "Ripping strings from binary with file offsets..."
        strings -a -t x $1 > $1.ltdis.strings.txt
        echo "Any strings found in $1 have been written to $1.ltdis.strings.txt with file offset"



else
        echo "Disassembly failed!"
        echo "Usage: ltdis.sh <program-file>"
        echo "Bye!"
fi
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ ./ltdis.sh -s "$1.ltdis.x86_64.txt"
zsh: permission denied: ./ltdis.sh
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ chmod +x ltdis.sh
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ ./ltdis.sh -s "$1.ltdis.x86_64.txt"
Attempting disassembly of -s ...
objdump: 'a.out': No such file
objdump: section '.text' mentioned in a -j option, but not found in any input file
Disassembly failed!
Usage: ltdis.sh <program-file>
Bye!
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ ./ltdis.sh static 
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$  cat static.ltdis.x86_64.txt

static:     file format elf64-x86-64


Disassembly of section .text:

0000000000000530 <_start>:
 530:   31 ed                   xor    %ebp,%ebp
 532:   49 89 d1                mov    %rdx,%r9
 535:   5e                      pop    %rsi
 536:   48 89 e2                mov    %rsp,%rdx
 539:   48 83 e4 f0             and    $0xfffffffffffffff0,%rsp
 53d:   50                      push   %rax
 53e:   54                      push   %rsp
 53f:   4c 8d 05 8a 01 00 00    lea    0x18a(%rip),%r8        # 6d0 <__libc_csu_fini>
 546:   48 8d 0d 13 01 00 00    lea    0x113(%rip),%rcx        # 660 <__libc_csu_init>
 54d:   48 8d 3d e6 00 00 00    lea    0xe6(%rip),%rdi        # 63a <main>
 554:   ff 15 86 0a 20 00       call   *0x200a86(%rip)        # 200fe0 <__libc_start_main@GLIBC_2.2.5>
 55a:   f4                      hlt
 55b:   0f 1f 44 00 00          nopl   0x0(%rax,%rax,1)

0000000000000560 <deregister_tm_clones>:
 560:   48 8d 3d d9 0a 20 00    lea    0x200ad9(%rip),%rdi        # 201040 <__TMC_END__>
 567:   55                      push   %rbp
 568:   48 8d 05 d1 0a 20 00    lea    0x200ad1(%rip),%rax        # 201040 <__TMC_END__>
 56f:   48 39 f8                cmp    %rdi,%rax
 572:   48 89 e5                mov    %rsp,%rbp
 575:   74 19                   je     590 <deregister_tm_clones+0x30>
 577:   48 8b 05 5a 0a 20 00    mov    0x200a5a(%rip),%rax        # 200fd8 <_ITM_deregisterTMCloneTable>
 57e:   48 85 c0                test   %rax,%rax
 581:   74 0d                   je     590 <deregister_tm_clones+0x30>
 583:   5d                      pop    %rbp
 584:   ff e0                   jmp    *%rax
 586:   66 2e 0f 1f 84 00 00    cs nopw 0x0(%rax,%rax,1)
 58d:   00 00 00 
 590:   5d                      pop    %rbp
 591:   c3                      ret
 592:   0f 1f 40 00             nopl   0x0(%rax)
 596:   66 2e 0f 1f 84 00 00    cs nopw 0x0(%rax,%rax,1)
 59d:   00 00 00 

00000000000005a0 <register_tm_clones>:
 5a0:   48 8d 3d 99 0a 20 00    lea    0x200a99(%rip),%rdi        # 201040 <__TMC_END__>
 5a7:   48 8d 35 92 0a 20 00    lea    0x200a92(%rip),%rsi        # 201040 <__TMC_END__>
 5ae:   55                      push   %rbp
 5af:   48 29 fe                sub    %rdi,%rsi
 5b2:   48 89 e5                mov    %rsp,%rbp
 5b5:   48 c1 fe 03             sar    $0x3,%rsi
 5b9:   48 89 f0                mov    %rsi,%rax
 5bc:   48 c1 e8 3f             shr    $0x3f,%rax
 5c0:   48 01 c6                add    %rax,%rsi
 5c3:   48 d1 fe                sar    $1,%rsi
 5c6:   74 18                   je     5e0 <register_tm_clones+0x40>
 5c8:   48 8b 05 21 0a 20 00    mov    0x200a21(%rip),%rax        # 200ff0 <_ITM_registerTMCloneTable>
 5cf:   48 85 c0                test   %rax,%rax
 5d2:   74 0c                   je     5e0 <register_tm_clones+0x40>
 5d4:   5d                      pop    %rbp
 5d5:   ff e0                   jmp    *%rax
 5d7:   66 0f 1f 84 00 00 00    nopw   0x0(%rax,%rax,1)
 5de:   00 00 
 5e0:   5d                      pop    %rbp
 5e1:   c3                      ret
 5e2:   0f 1f 40 00             nopl   0x0(%rax)
 5e6:   66 2e 0f 1f 84 00 00    cs nopw 0x0(%rax,%rax,1)
 5ed:   00 00 00 

00000000000005f0 <__do_global_dtors_aux>:
 5f0:   80 3d 49 0a 20 00 00    cmpb   $0x0,0x200a49(%rip)        # 201040 <__TMC_END__>
 5f7:   75 2f                   jne    628 <__do_global_dtors_aux+0x38>
 5f9:   48 83 3d f7 09 20 00    cmpq   $0x0,0x2009f7(%rip)        # 200ff8 <__cxa_finalize@GLIBC_2.2.5>
 600:   00 
 601:   55                      push   %rbp
 602:   48 89 e5                mov    %rsp,%rbp
 605:   74 0c                   je     613 <__do_global_dtors_aux+0x23>
 607:   48 8b 3d fa 09 20 00    mov    0x2009fa(%rip),%rdi        # 201008 <__dso_handle>
 60e:   e8 0d ff ff ff          call   520 <__cxa_finalize@plt>
 613:   e8 48 ff ff ff          call   560 <deregister_tm_clones>
 618:   c6 05 21 0a 20 00 01    movb   $0x1,0x200a21(%rip)        # 201040 <__TMC_END__>
 61f:   5d                      pop    %rbp
 620:   c3                      ret
 621:   0f 1f 80 00 00 00 00    nopl   0x0(%rax)
 628:   f3 c3                   repz ret
 62a:   66 0f 1f 44 00 00       nopw   0x0(%rax,%rax,1)

0000000000000630 <frame_dummy>:
 630:   55                      push   %rbp
 631:   48 89 e5                mov    %rsp,%rbp
 634:   5d                      pop    %rbp
 635:   e9 66 ff ff ff          jmp    5a0 <register_tm_clones>

000000000000063a <main>:
 63a:   55                      push   %rbp
 63b:   48 89 e5                mov    %rsp,%rbp
 63e:   48 8d 3d a3 00 00 00    lea    0xa3(%rip),%rdi        # 6e8 <_IO_stdin_used+0x8>
 645:   e8 c6 fe ff ff          call   510 <puts@plt>
 64a:   b8 00 00 00 00          mov    $0x0,%eax
 64f:   5d                      pop    %rbp
 650:   c3                      ret
 651:   66 2e 0f 1f 84 00 00    cs nopw 0x0(%rax,%rax,1)
 658:   00 00 00 
 65b:   0f 1f 44 00 00          nopl   0x0(%rax,%rax,1)

0000000000000660 <__libc_csu_init>:
 660:   41 57                   push   %r15
 662:   41 56                   push   %r14
 664:   49 89 d7                mov    %rdx,%r15
 667:   41 55                   push   %r13
 669:   41 54                   push   %r12
 66b:   4c 8d 25 46 07 20 00    lea    0x200746(%rip),%r12        # 200db8 <__frame_dummy_init_array_entry>
 672:   55                      push   %rbp
 673:   48 8d 2d 46 07 20 00    lea    0x200746(%rip),%rbp        # 200dc0 <__do_global_dtors_aux_fini_array_entry>
 67a:   53                      push   %rbx
 67b:   41 89 fd                mov    %edi,%r13d
 67e:   49 89 f6                mov    %rsi,%r14
 681:   4c 29 e5                sub    %r12,%rbp
 684:   48 83 ec 08             sub    $0x8,%rsp
 688:   48 c1 fd 03             sar    $0x3,%rbp
 68c:   e8 57 fe ff ff          call   4e8 <_init>
 691:   48 85 ed                test   %rbp,%rbp
 694:   74 20                   je     6b6 <__libc_csu_init+0x56>
 696:   31 db                   xor    %ebx,%ebx
 698:   0f 1f 84 00 00 00 00    nopl   0x0(%rax,%rax,1)
 69f:   00 
 6a0:   4c 89 fa                mov    %r15,%rdx
 6a3:   4c 89 f6                mov    %r14,%rsi
 6a6:   44 89 ef                mov    %r13d,%edi
 6a9:   41 ff 14 dc             call   *(%r12,%rbx,8)
 6ad:   48 83 c3 01             add    $0x1,%rbx
 6b1:   48 39 dd                cmp    %rbx,%rbp
 6b4:   75 ea                   jne    6a0 <__libc_csu_init+0x40>
 6b6:   48 83 c4 08             add    $0x8,%rsp
 6ba:   5b                      pop    %rbx
 6bb:   5d                      pop    %rbp
 6bc:   41 5c                   pop    %r12
 6be:   41 5d                   pop    %r13
 6c0:   41 5e                   pop    %r14
 6c2:   41 5f                   pop    %r15
 6c4:   c3                      ret
 6c5:   90                      nop
 6c6:   66 2e 0f 1f 84 00 00    cs nopw 0x0(%rax,%rax,1)
 6cd:   00 00 00 

00000000000006d0 <__libc_csu_fini>: 
 6d0:   f3 c3                   repz ret
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ cat static.ltdis.strings.txt             
    238 /lib64/ld-linux-x86-64.so.2
    361 libc.so.6
    36b puts
    370 __cxa_finalize
    37f __libc_start_main
    391 GLIBC_2.2.5
    39d _ITM_deregisterTMCloneTable
    3b9 __gmon_start__
    3c8 _ITM_registerTMCloneTable
    660 AWAVI
    667 AUATL
    6ba []A\A]A^A_
    6e8 Oh hai! Wait what? A flag? Yes, it's around here somewhere!
    7c7 ;*3$"
   1020 picoCTF{d15a5m_t34s3r_ae0b3ef2}
   1040 GCC: (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.0
   1671 crtstuff.c
   167c deregister_tm_clones
   1691 __do_global_dtors_aux
   16a7 completed.7698
   16b6 __do_global_dtors_aux_fini_array_entry
   16dd frame_dummy
   16e9 __frame_dummy_init_array_entry
   1708 static.c
   1711 __FRAME_END__
   171f __init_array_end
   1730 _DYNAMIC
   1739 __init_array_start
   174c __GNU_EH_FRAME_HDR
   175f _GLOBAL_OFFSET_TABLE_
   1775 __libc_csu_fini
   1785 _ITM_deregisterTMCloneTable
   17a1 puts@@GLIBC_2.2.5
   17b3 _edata
   17ba __libc_start_main@@GLIBC_2.2.5
   17d9 __data_start
   17e6 __gmon_start__
   17f5 __dso_handle
   1802 _IO_stdin_used
   1811 __libc_csu_init
   1821 __bss_start
   182d main
   1832 __TMC_END__
   183e _ITM_registerTMCloneTable
   1858 flag
   185d __cxa_finalize@@GLIBC_2.2.5
   187a .symtab
   1882 .strtab
   188a .shstrtab
   1894 .interp
   189c .note.ABI-tag
   18aa .note.gnu.build-id
   18bd .gnu.hash
   18c7 .dynsym
   18cf .dynstr
   18d7 .gnu.version
   18e4 .gnu.version_r
   18f3 .rela.dyn
   18fd .rela.plt
   1907 .init
   190d .plt.got
   1916 .text
   191c .fini
   1922 .rodata
   192a .eh_frame_hdr
   1938 .eh_frame
   1942 .init_array
   194e .fini_array
   195a .dynamic
   1963 .data
   1969 .bss
   196e .comment
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ cat static.ltdis.strings.txt | grep "picoCTF"
   1020 picoCTF{d15a5m_t34s3r_ae0b3ef2}
                                                                        
┌──(kali㉿kali)-[~/Documents/retosCTF]
└─$ 

Respuesta: picoCTF{d15a5m_t34s3r_ae0b3ef2}

*** 

## Notas Adicionales

## Referencias

https://www.youtube.com/watch?v=cVpei_-wGMQ&ab_channel=AlmondForce