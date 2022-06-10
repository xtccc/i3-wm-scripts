i3-wm-scripts
=============

i3 Window Manager Scripts

These are python scripts that read/write to i3 using i3-msg. By using regular expressions it is possible to 
search for windows with particular names and jump to them. 

Dependencies: i3, i3-msg (distributed with i3), rofi

There are 4 scripts: nextmatch, nextfind, goto, mark

### nextfind

Syntax: nextfind

This script provides a rofi list of arguments. If you select one a window that is active
and there are multiple with the same name then it jumps to the next one,
otherwise it stays at the current.

Example Binding:
```
bindsym $mod+e exec python ~/.config/i3/nextfind # use rofi to select an open window
```
demo:
![demo](./demo.gif)

### Install
To install just put the scripts in your path, or bind the scripts in you config
file.

```
cp common.py nextfind ~/.config/i3/
```
