# EBSL
EBSL (EasyByteScratchLang) is a programing language used to communicate with the 8 bit computer emu (v2 is the latest).
For usage examples visit folders in all uppercase like 'BLINKY' and import (Right click on list) your Program.txt to the Program list.
Check INSTRUCTIONS.md for all instructions and syntax. Curently there are 56 instructions.

# Run EBSL
Open the offline scratch editor and import emu-v2.sb3
Turn on turbo mode by clicking edit and you should see it in the dropdown.
Now you can set any hz you want or run it at full speed!
For latest updates go to https://scratch.mit.edu/projects/1287676122/

[Turbo warp link with recomended settings (60fps, turbo)](https://turbowarp.org/1287676122?fps=60&turbo)
# Deafult specs
These are the default specs of the computer emu:
1. 60 hz cpu (full speed on turbo mode)
2. 16 bytes of ram.
3. 48 bytes of storage.
4. 18 buttons total. (range 1-18)
5. 12x5 LED display (range 1-60)

# Examples of EBSL
These are the most basic examples of EBSL, for more look in the folders titled what programs they are.
```
LEDON 1
DELAY 200
LEDOFF 1
RETURN Ok
HALT
// Turns led 1 on, then waits 200ms, then turns it off, then sets RETURN (aka as the program status, can be used for diffrent things too, and isnt needed) then waits forever
```
```
INPUT
EQUALS cache 1 1
// Is the user input equal to 1, save result to bit 1
CONDJUMP 5 7 1
BEEP
HALT
LEDON 1
DELAY 200
LEDOFF 1
DELAY 200
JUMP 7
// If bit 1 is 1, beeps and halts, else jumps to a forever blinking led loop

// Explanation:
// We compare the cache to the built in value, you can replace the 1 to anything, 
// just not the second 1, second 1 is the ram adress (example: "EQUALS cache example-value 1")
// After we compare and save the comparision value, we run CONDJUMP, CONDJUMP jumps to the line 5 if the bit number 1 is
// 1, else it jumps to line 7, 5 is the line for beep, and 7 is the ledon loop.

// Expected behavior:
// If the user inputs 1, the device should beep and halt, if the user inputs something diffrent, it will run a led blinking loop
```
Code automaticly loops, you can use HALT to stop it or use JUMPs (and CONDJUMPs).

### Py2EBSL
Theres a html app in this repo called py2ebsl.html basicly you can convert basic python to ebsl.
[Py2EBSL](https://simonko-912.github.io/EBSL/py2ebsl.html)
