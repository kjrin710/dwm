[中文版](./docs/README_zh.md)  

# dwm - Dynamic Window Manager

Dwm is an X system window manager with extremely fast performance, small size, and flexible functions.  
The configuration of dwm is achieved by creating a custom config.h file and recompiling the source code.  
This is the personal branch of the [dwm](https://dwm.suckless.org/) project, which originated from [suckless.org](https://suckless.org/)   

## Requirements/Conditions

To build dwm, you need the Xlib header files.  

## Installation

Modify the config.mk file to suit your local environment settings (by default, dwm is installed in the /usr/local directory).  
Then, enter the following command to build and install dwm (please execute it as root if necessary):  

`make clean install`  

## Run dwm

Add the following content to your .xinitrc file, and you can start dwm by using the startx command:  

`exec dwm`  

If you want to connect the dwm to the specified display, make sure that the DISPLAY environment variable has been set correctly, for example:  

`DISPLAY=foo.bar:1 exec dwm`  

(This will cause dwm to start on display :1 of the host foo.bar)   

## Custom Configuration

The following personalized adjustments have been made on the basis of the original dwm:  

### Patch 
- actualfullscreen
- hide vacant tags
- pertag
- status2d-systray
- fullscreen

### Appearance
- **Font**: Use `fontawesome`, size 16
- **Theme**: Dark blue color scheme

### Shortcut Changes
- **Modifier Key**: The default modifier key ALT (Mod1) is replaced with Super (MOD4) key
- **New Key Positions**:
- Increase/Decrease amixer volume: `Super + Shift + ↑ / ↓`
- Full-screen screenshot with Flameshot: `Super + s`
- Flameshot GUI: `Super + Shift + s`
- **Adjust Key Positions**: 
- Start terminal: `Super + Shift + Return` -> `Super + Return`
- Zoom: `Super + Return` -> `Super + Shift + Return`
- Close current window: `Super + Shift + c` -> `Super + q`
- Exit dwm: `Super + Shift + q` -> `Super + Shift + c`  
Other default shortcuts remain unchanged. Refer to the config.h configuration file for details.
