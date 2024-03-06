# How to use
Create a new file (in the web interface like mainsail) called customized.cfg and put all the contents from 'customized' in it. Then add '[include customized.cfg]' to the printer.cfg (if you don't have one then try to find one in the config examples).

![image](https://github.com/Pigensworth/Ender-3-or-3-pro-Klipper-printer.cfg/assets/136399546/49a9e94d-1046-4306-ae53-e3960f0ec464)


# BLTouch/CRTouch
If using a BLTouch/CRTouch, uncomment everything between the emojis in the 'customized' file, change the pin for the endstop_pin to 'probe:z_virtual_endstop', and replace 'position_endstop: 0.0' with 'position_min: -5'.

![image](https://github.com/Pigensworth/Ender-3-or-3-pro-Klipper-printer.cfg/assets/136399546/16c26fe0-550d-4519-a990-4565728e6357)

# Screen
If you want my screen layout customization, then copy everything from the 'Screen' file and paste it at the end of the 'customized' file.
