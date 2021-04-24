# Linux_Kernal
Making Operting System Linux kernal

selvaraj@selvaraj-ubuntu:~/kernal$ ls                                                                                                                                   
boot.asm  grub.cfg  kernel.c  linker.ld

COMPILATION TIME
Build the boot.asm into an object file
selvaraj@selvaraj-ubuntu:~/kernal$ nasm -f elf32 boot.asm -o boot.o

Build the kernal.c into an object file
selvaraj@selvaraj-ubuntu:~/kernal$ gcc -m32 -c kernel.c -o kernel.o

Link both object files and create the executable program(kernal)
selvaraj@selvaraj-ubuntu:~/kernal$ ld -m elf_i386 -T linker.ld -o kernel boot.o kernel.o




