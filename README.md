# How to use
Create a new file (in the web interface like mainsail) called customized.cfg and put all the contents from 'customized' in it. Then add '[include customized.cfg]' to the printer.cfg (if you don't have one then try to find one in the config examples).

![image](https://github.com/Pigensworth/Ender-3-or-3-pro-Klipper-printer.cfg/assets/136399546/49a9e94d-1046-4306-ae53-e3960f0ec464)


# BLTouch/CRTouch
If using a BLTouch/CRTouch, uncomment everything between the emojis in the 'customized' file, change the pin for the endstop_pin to 'probe:z_virtual_endstop', and replace 'position_endstop: 0.0' with 'position_min: -5'.

![image](https://github.com/Pigensworth/Ender-3-or-3-pro-Klipper-printer.cfg/assets/136399546/16c26fe0-550d-4519-a990-4565728e6357)

# Screen
If you want my screen layout customization, then copy everything from the 'Screen' file and paste it at the end of the 'customized.cfg' file. It disables the Octoprint section (since I don't use Octoprint), shows the tune section and start print all the time, adds a cancel print, and changes the cooldown from a list of cooldown heater, cooldown bed, and cooldown all to simply cooldown all.

# Slicer Start & End
This is what to put in the slicer start g-code and end g-code. It's for Cura because that's what I use, so it would probably work with Creality Slicer or any others based off of Cura, but I don't know if it works with anything else. If you get an error like "Error evaluating 'gcode_macro START_PRINT:gcode': jinja2.exceptions.UndefinedError: 'dict object' has no attribute 'BED'", that means there's something wrong with the start g-code, because the slicer isn't passing the value of the variables to the g-code and therefore to Klipper.

# Presets
I put on a preset for the 4.2.7 board (the silent one) with a BLTouch, and one for the 4.2.2 (the loud one that I think is on the Ender 3) without a BLTouch. Neither of them have the screen layout mod, but they both have my customization. I don't know for sure if the 4.2.2 one works, because I found mixed pin mappings for it, but neoyagami used it, so it should work. Thanks to neoyagami for his config file, that's what the 4.2.2 is based on. His can be found at https://gist.github.com/neoyagami/5f431928997dbf255e84e4c937983e8e.
