## SCP/DOS: A simple 64-bit operating system!
Welcome to SCP/DOS, an operating system from yesteryear, brought into the world of today. 

The purpose of this operating system was simple: To provide users with a user experience and programming environment identical to that which MS-DOS 3.30 provided users back in the mid to late 1980s. 
This operating system was developed completely in x86-64 assembly, with an API comparible to that which programmers would have had access to back in the wonderful days of DOS. Thats right, its Int 21h all the way down! 
Furthermore, from a users perspective one would be hard pushed to believe that this is anything but an OS from the 1980's, right up to the messages COMMAND.COM will throw up at you. Oh yes, be prepared to say hello to your old friend "ABORT, RETRY, IGNORE, FAIL?"!!

Due to the move to 64-bits, some concessions needed to be made and unfortunately some features of DOS which had their origins in CP/M are now considered obsoleted. A full list will be provided in the programmers and users guides which will detail how to use SCP/DOS. However, those features which did remain, have been given a fresh lick of paint in the form of being brought up to speed with the modern world:
- The operating system is fully 64-bit.
- Can handle files up to 4Gb in size (and even larger on redirector drives).
- Has provisions for preemptive multitasking (though the multitasker module is not yet ready).
- Has full support for PE executables and .COM style executables.
- Has native support for FAT12/16/32 (currently without long file names).
- Extends the DOS device driver model.
- Has support for the network redirector (REDIR) and thus Installable File Systems (IFS).
- Has support for almost all undocumented DOS endpoints including the complete 2F/12xxh line of internal function calls.
- Supports full IO redirection.
- And many other features, including new Int 21h endpoints!

In effect, if one has a reference sheet of the API endpoints of DOS 3.3, then one has a reference sheet of the majority of the SCP/DOS endpoints. Therefore, it is recommended that when writing a program for SCP/DOS, one becomes familiar with the 
Ralf Brown Interrupt List (RBIL). 

Therefore, if you like MS-DOS and want to see it live well into the 21st century, even past the UEFI takeover, I emplore you to give SCP/DOS a try! 
It is frequently tested on compatible hardware to ensure that any changes to the operating system and file system drivers don't ruin hardware compatibilty. 

Hardware requirements for SCP/DOS include:
- An x86-64 processor.
- 2Mb of RAM or higher.
- VGA compatible graphics chipset.
- CSM or BIOS compatible motherboard.
- One or two USB EHCI buses.
- ATA based hard drives (in IDE mode).
- PS/2 keyboard.

For full details, please see the following repository: https://github.com/ybuzoku/SCP-BIOS

If you have any questions or would like to get involved please get in contact with me here or at ybuzoku<AT>hotmail.co.uk.

Some projects for which I would be enternally grateful if one could contribute include:
- A UEFI bootloader for SCP/DOS, that works by hooking directly into the SYSINIT module.
- UEFI support in the disk manipulation utilities.
- Rewriting the default disk driver to be compatible with 2Fh/08xxh and hook into the disk io interrupts properly.
- Multitasker (DOSMGR).
- DLL manager (DLLMAN).
- An installer for Windows/*nix based systems.
- Porting compilers/assemblers.
- Writing an MS-DOS compatible ANSI.SYS driver.
- Writing an exFAT IFS.

For all aforementioned tasks, I would be more than happy to liase and co-develop. Most of these tasks are already in the works in any case.

# What about applications?

SCP/DOS currently has a few applications which highlight the usability of the system. These include:
- COMMAND.COM - An amazing command interpreter.
- EDLIN.COM - A line editor.
- FDISK.COM - A _proper_ disk formatting utility (MBR only for now).
- FORMAT.COM - A disk formatting utility.
- SYS.COM - An operating system installation ultility.
- MORE.COM - An IO filter for pagination.
- LABEL.COM - A disk label editor.
- FC.EXE - A demonstration file comparison program written in C.
- RDEBUG.COM - A program which depends on SCP/BIOS to launch the system debugger.
- INTBASIC.COM - A buggy port of INTBASIC, the SCP/BIOS demonstration BASIC program.

Whilst these don't exactly form an exciting set of programs, they demonstrate the ability of DOS to be a usable operating system as they highly the functionality of the operating system to a user.

# So thats it! 

Welcome to the world of friendly computing once more!

All the best,

Yll@SCP/DOS
