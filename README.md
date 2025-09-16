# DWM_optim
This is a DWM's fork with less features and some improvments.See the https://suckless.org/dwm/ for original dwm.

dwm is an extremely fast, small, and dynamic window manager for X.


Requirements
------------
1. In order to build dwm you need the Xlib header files.
2. For compiling I use TCC (tcc package). Read Installation for instructions how to change this
3. Other standard utilities: dmenu, rofi, st, flameshot. Read TODO please.


Installation
------------
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default). There

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.

Deleted/added features
-------------
+ Added keybind for screenshots
+ Added keybinds for increasing/decreasing volume

- Deleted some functions from original dwm.


Goal
-------------
The long-term goal is to make it smaller than 2000 lines. Read TODO please
