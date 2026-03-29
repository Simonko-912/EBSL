# EBSL
EBSL (EasyByteScratchLang) is a programing language used to communicate with the 8 bit computer emu (v2 is the latest).
For usage examples visit folders in all uppercase like 'BLINKY' and import (Right click on list) your Program.txt to the Program list.
Check INSTRUCTIONS.md for all instructions and syntax. Curently there are 56 instructions.

# Run EBSL
Open the offline scratch editor and import emu-v2.sb3
Turn on turbo mode by clicking edit and you should see it in the dropdown.
Now you can set any hz you want or run it at full speed!
For latest updates go to https://scratch.mit.edu/projects/1287676122/

# Deafult specs
These are the default specs of the computer emu:
1. 60 hz cpu (full speed on turbo mode)
2. 16 bytes of ram.
3. 48 bytes of storage.
4. 18 buttons total. (range 1-18)
5. 12x5 LED display (range 1-60)

# Example of EBSL
This is the most basic example of EBSL, for more look in the folders titled what programs they are.
```
LEDON 1
DELAY 200
LEDOFF 1
RETURN Ok

```

This code automaticly loops, you can use HALT to stop it or use JUMPs (and CONDJUMPs).

### Py2EBSL
Theres a html app in this repo called py2ebsl.html basicly you can convert basic python to ebsl.
