# My ST(simple terminal) Build

Super lighweight and fast

## Instalation
clone and ```make clean install```

## patches
* alpha
* xresources
* vim-browser

## changing color scheme
you can change the color scheme by changing ~/.Xresources file
this is a example of a color scheme

```
!! Transparency (0-1):
st.alpha: 0.1

!! Set a default font and font size as below:
st.font: Liberation Mono-15;

! st.termname: st-256color
! st.borderpx: 2

!! Set the background, foreground and cursor colors as below:

/* !! solarized */
*.color0:	#073642
*.color1:	#dc322f
*.color2:	#859900
*.color3:	#b58900
*.color4:	#268bd2
*.color5:	#d33682
*.color6:	#2aa198
*.color7:	#eee8d5
*.color9:	#cb4b16
*.color8:	#fdf6e3
*.color10:	#586e75
*.color11:	#657b83
*.color12:	#839496
*.color13:	#6c71c4
*.color14:	#93a1a1
*.color15:	#fdf6e3
```
## Reload xresources
you need xrdb to reload xresources, just run
```
xrdb ~/.Xresources
```
restart your terminal and your changes will take effect

## hotkeys
alt+c is vim-browse
ctrl+c in vim copy to clipboard
to copy from the terminal output use vim-browse, yank to copy to clipboard
alt+shift+v paste on the terminal from the clipboard

## Extra info

Requirements
------------
In order to build st you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

