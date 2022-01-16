# Floppy2Arduino2USB
PCB to connect a floppy drive to a Arduino Nano and (ultimately) to a modern personal computer over USB (FTDI). 

This PCB is an implementation of Rob Smith's project "Arduino Amiga Floppy Disk Reader/Writer aka DrawBridge" that connects a vintage floppy drive to a modern personal computer in order to allow the modern computer to read floppy disks written by Amiga computers.

The original idea for the project, which is the basis of this PCB, is by Rob Smith (https://amiga.robsmithdev.co.uk/).

The original idea for the hardware design as well as the software that is needed to use the hardware are all copyright by Rob Smith. Any licences that he has attached to his project / ideas / software apply! Please visit his website for mor information before using this files (https://amiga.robsmithdev.co.uk/).

===>  A huge "thank you" to Rob Smith for the creation of this awful project!! <===

The license I included with the gerbers on this repository only apply to my special implementation of the project.

In my implementation, I included a voltage regulator (12V input to 5V output) to power the Arduino. The 5V power for the disk drive comes directly from the external power connector and is routed directly to the drive. I included the voltage regulator for no particular reason - I just wanted to implement a voltage regulator as an exercise. The deeper idea was, that in doing so, the Arduino and the drive will get their powers from separate rails without disturbing each other too much.

In the default configuration, only 5V but no 12V is routed to the floppy drive. If your floppy does need 12V, a jumper can be set to deliver 12V to the drive, too. The 12V rail will be shared between the voltage regulator on the pcb and the drive in that scenario, however. Please do also note, that this scenario is untested by me, as my drive does not need 12V. Use this variant at your own risk.

In hindsight, I should have taken the 12V rail from the external power for both the 5V and the 12V for the floppy drive and use the 5V rail of the external power directly for the Arduino. But whatever: It works for me, as it is, so I did not change it nor did I order a new batch to test it. Feel free to change the design to your needs, if you want.

Warning:
I have tested the design found in this repository with my own equipment and it does work as intended. I am a hobbyist, however, without any deeper knowledge of pcb design so beware: I cannot and I do not give any warranty that it will work for you on your equimpment nor that it won't damage anything by using it. The files are provided "as it is" - use them on your own risk.
