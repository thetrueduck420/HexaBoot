a second stage bootloader for the raspberry pi pico and arduino

this works on pretty low memory and flash, its relativelly small and it includes a filesystem called betterfs, made by me, in order to load an OS, you must put your os in a function

example(){

 Serial.println("this is a testing os");

}

then you must add it to the BOOT_OS array and change the buffer (default being 1 for restart)

then you need to add its name in the BOOT_BOOTABLE list, the code is very commented so dont worry about making mistakes

once starting, the bootloader lists every bootable os and executes it

you must code the os yourself, or get one from github like freeRTOS
in addition, you can also add my PIgrade repo, which is linux for arduino
its specifically built for this filesystem and bootloader

do you have an sd card?
good
you dont have to do all of this

just select the "sd card" os, wait for it do do its thing and turn it off

then, youre gonna find a folder called "operating-systems" on the sd card

in it, youre gonna want to put an assembled os
one is provided 
the one provided is an assembler, select an assembly file and itll assemble it
then you can put it inside of the "operating-systems" folder and you can now boot into it!

assembly documentation is available in this repo


feel free to add issues if you have any, id love to answer, it makes me feel pretty damn smart

