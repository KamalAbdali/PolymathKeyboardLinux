US-POLYMATH KEYBOARD LAYOUT FOR LINUX

To activate this keyboard, you have to
 
i) add some files from here into the directory 'xkb' in your 
   system, 
ii) execute a compile command, and then 
iii) change some system settings on your machine so that your 
   typed input can make use of the new keyboard layout.
 
The first two actions require superuser priviliges to execute
'su' or 'sudo' command.

The steps needed to install and use US-Polymath keyboard layout
are the following:

1. Download the file US-PolymathLnx.zip and unzip it into some 
local directory, e.g. 'US-PolymathLnx'. 

2. Find the path to 'xkb' in your system. In most distributions 
of Linux, this path is '/usr/share/X11/xkb', but your installation 
might not use this standard path. You can determine the path for 
your machine by executing the 'find' command, as follows:
	find / -name xkb -print
The example commands below use the standard location. 

3. Become a superuser, by executing the command 
	su
You would be required to type in the root password.

4. Backup the five files that are going to be replaced.
	cd /usr/share/X11/xkb/symbols
	mv us us.bak
	cd ../rules
	mv base.lst base.lst.bak
	mv evdev.xml evdev.xml.bak
	mv xorg.lst xorg.lst.bak
        cd ../types
        mv extra extra.bak

5. Place five new files in the system. The example commands
below assume that the files have been downloaded into a
directory called 'US-PolymathLnx' and the path to 'xkb' is
'/usr/share/X11/xkb'.

	cd US-PolymathLnx/symbols
	cp us /usr/share/X11/xkb/symbols/
	cd ../rules
	cp base.lst evdev.xml xorgs.lst /usr/share/X11/xkb/rules/
	cd ../types
	cp extra /usr/share/X11/xkb/types/

6. Execute the following command to compile the changed
keyboard information into the system:

   setxkbmap -layout us -variant us-polymath -print | xkbcomp -

(For this command to work, you might need to be in an Xterm
 shell window rather than a regular command window, and
 again execute 'su' command first.)

7. Logout and login again (or restart the machine) for the
above changes to take effect.

8. To make use of the US-Polymath keyboard layout in your
input, you have to change some system settings. Depending on
which Linux distribution and desktop interface you are using,
this might require typing special commands or, with the more
convenient graphics interface, working with 'System Settings,
'Control Panel', etc. 

The following example is for OpenSUSE distribution and KDE
desktop.

A. From the 'Application Launcher', select 'Settings', then 
'Configure Desktop'. From the 'Hardware' section, select 
'Input Devices'. It will display the 'Keyboard ...' panel. 
Click on 'Layout' tab.

B. In the lower pane 'Configure Layouts', click on the 'Add'
button, and from the choices displayed, select Map 'us', 
Layout 'English (US)', Variant 'English (polymath ...)'.

C. Go to the upper pane of 'Layouts' tab. In the
'Layout indicator', select 'Show layout indicator' and
'Show flag'. In 'Switching Policy', select 'Global'.
In 'Shortcuts for Switching Layout', select 'Alt+Shift' for
'Main shortcuts'. 
(This --- to get you started --- is just one set of suitable
choices among several alternatives.)

D. Click on 'Apply'.

In the panel area you should now see a flag to indicate the
active keyboard layout (US flag for the us-polymath layout).
If you have several keyboard layouts installed, then Shift-ALT
should toggle among them.

