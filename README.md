PC/SC APDU inspection and manipulation tool (APDUPlay)
========

PC/SC inspection and manipulation tool


The project APDUPlay is based on ApduView tool (http://www.fernandes.org/apduview/index.html) which allows you to log communication realized via PC/SC interface (winscard.dll library). If you are interested only in log of transmitted data, you can readily
use APDUView project (although APDYPlay project provides information about communication in more structured way more suitable for later post processing and add some additional information).

Note: The APDUPlay tool is available for download including source codes, yet documentation still lack a bit behind :(. Still, it was requested several times and I hope it will be useful.

How to use it?
1. Copy Winscard.dll from your system folder (see note below to select correct version) to folder with target application and rename it to original.dll
2. Copy Winscard.dll from APDUPlay project to folder with target application (see download below)
3. Run application and inspect resulting files winscard_log.txt and winscard_rules_log.txt
4. (Optional) Change configuration file winscard_rules.txt to modify default behaviour (see below)

APDUPlay project provides winscard.dll library that is stub used instead of original winscard.dll provided by Microsoft. For correct usage, you need to find  Microsoft's library and copy it to folder with application you are trying to control with APDUPlay. 

If you are using Windows XP or Windows 7 32bit, you can find it at c:\Windows\winscard.dll

If you are using Windows 7 64bit, you can find it at c:\Windows\SysWOW64\winscard.dll

NOTE: If you will use (wrongly) 64bit version of library winscard.dll, it will fail with "The procedure entry point original.g_rgSCardT1Pci could not be located in the dynamic link library WinSCard.dll."  

Please send me any comments or found bugs to the mail written at the footer of this page. 

The APDUPlay project is providing following functionality: 
  * Log content and additional information about exchanged PC/SC communication
  * Manipulate communication in real time
  * Redirect communication via socket to other device/computer
  * Reorder list of smart card readers detected in a system
  * Visualize captured data in structured way by GraphViz

See more details at https://github.com/petrs/APDUPlay/wiki.

