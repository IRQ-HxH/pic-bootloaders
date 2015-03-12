# Introduction #

This is a list of all the available Microchip PIC bootloaders and major features.

# Desirable boot loader properties #

For a bootloader to be useful in a commercial project, there are a number of properties that it should have:

  * boot loader runs from the PIC boot block which can be protected (this helps ensure the bootloader never becomes corrupted)
  * PIC Source code should be available (otherwise it can't be ported to new PICs, different baud rates, etc)
  * PC side source code should be available (so you can produce a professional looking firmware upgrade tool or alter it if there is a special way to enter the bootloader on your product)
  * The bootloader should run briefly when the PIC boots (so that you can recover if the underlying application has been corrupted)
  * The data written should be verified

Obviously, ideally, it should be free too.

# Our bootloader #

You can find the bootloader and PC app that we use with PIC18F2550 chips by clicking the "Downloads" or "Source" tabs at the top of the page. It is based on the tiny bootloader, and uses the same protocol. The PC app has been written from scratch in portable C.

# Details of other bootloaders for Microchip PICs #

http://www.etc.ugal.ro/cchiculita/software/picbootloader.htm - tinyboot loader: good, but PC app source code not available

http://forum.microchip.com/tm.aspx?m=126770 - wombat encrypted serial: very good, but you need a C compiler for the PIC

http://www.fatih.edu.tr/~onur/PIC18F452/Colt%20Bootloader/Colt%20PIC18F%20Bootloader%20Page.htm - Colt bootloader - good, but no source code available for PIC or PC

http://mrmackey.no-ip.org/elektronik/ds30loader/ - good. GPL licensed but can be used with closed-source/commercial firmware, all source provided, supports wide range of PICs.

http://www.microchip.com/stellent/idcplg?IdcService=SS_GET_PAGE&nodeId=1824&appnote=en012031 - microchip an851 - good, but PC app is in obsolete Visual Basic 6.0 and bootloader doesn't run when PIC boots.

http://www.microchip.com/stellent/idcplg?IdcService=SS_GET_PAGE&nodeId=1824&appnote=en546974 - microchip AN1310 - now looks very good, though should not be used with code protection as it will allow the firmware to be read out

http://picloader.cvs.sourceforge.net/viewvc/picloader/bootloader/ - usb bootloader, encryption support



# Related applications #

http://piklab.wiki.sourceforge.net/Command-line+Utility+ - can talk to various bootloaders

http://tinybldlinux.sourceforge.net/what.html - linux command line loader for tiny boot loader

# Other lists of Microchip PIC bootloaders #

http://mcuee.blogspot.com/2007/11/i-am-trying-to-collect-list-of.html

http://www.etc.ugal.ro/cchiculita/software/picbootloader.htm

http://www.piclist.com/techref/microchip/devprogs.htm#bootloaders

http://www.microchip.com/forums/tm.aspx?m=424874