US-POLYMATH KEYBOARD LAYOUT FOR LINUX

This is a fairly general-purpose keyboard meant to facilitate 
typing literary as well as scientific texts. It provides 
a variety of "combining diacritical marks" to type 
"extended characters" of Latin script. ("Extended characters" 
are composed by decorating ordinary letters of the alphabet 
with various accents and diacritical marks.) The keyboard also 
includes several math symbols, especially those commonly used 
in logic, set theory, and number theory, and the most frequently 
used Greek letters. 

To type extended characters, most other currently available 
keyboard layouts provide one of two alternative methods 
(sometimes a bit of each). In one method, "dead keys" are assigned 
to the modifying marks or accents. To type an extended character, 
you first press the dead key and then press the character to be 
modified.  In the alternative method, you first press the letter 
to be modifed, and then press the special key assigned to the 
combining diacritical mark. The US-Polymath Keyboard, by contrast, 
uses the second method exclusively.

How the extended characters are rendered and processed depends 
on the application receiving the text and the font used. In my own 
limited experimentation, the combination LibreOffice + STIX fonts 
has worked out the best.

The file "US-PolymathKeyboardWinLnx.pdf" (in the "distrib"
directory below) is a printable one-page keyboard map 
for reference.

*** DIRECTORIES ***

1. src

This directory contains three subdirectories: rules, symbols,
and types. The files in these subdirectories have to replace 
certain Linux system files, as explained in the file 
'readme-linux.txt' included in the directory 'distrib' below.

- Linux keyboard layout source file 'us' 
(in the subdirectory 'symbols').
This file contains several layout variants for the layout 'us'. 
The variant we need is labeled 'us-polymath'.

- The files 'base.lst', 'evdev.xml', and 'xorg.lst' (all in 
the subdirectory 'rules') needed to add the new layout to 
the xkb datbase.

- The file 'extra' (in the subdirectory 'types').
It contains several type definitions, the type that we need is 
"FOUR_LEVELS_PLUS_LOCK_PLUS_SHIFTLOCK'.

- TeX source file UrduQWERTYkeyboardWinLnx.tex. It should 
be processed by the XeLaTeX engine to produce the keymap
picture UrduQWERTYkeyboardWinLnx.pdf.


2. distrib

- This directory contains the files needed for installing
the US-Polymath keyboard layout on a Linux computer. It also 
includes a file 'readme-linux.txt' providing installation 
instructions and a keyboard map. 

- A zip of the files in this directory is a convenient way
to distribute the layout. Such a zip file is downloadable
from http://geomete.com/ftp/US-PolymathLnx.zip

