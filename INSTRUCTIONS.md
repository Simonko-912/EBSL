# The list of INSTRUCTIONS for EBSL

```
NOP = does nothing, small pause
HALT = wait forever, for debuging
DELAY x = waits x number of ms (one ms = 0.001 seconds)
LEDON x = turns the led number x on
LEDOFF x = turns the led number x off
SETRAM1 x = sets the bit x in ram to 1
SETRAM0 x = sets the bit x in ram to 0
SETLED x y = sets led x to y (y can be 1 or 0)
SETRAM x y = sets ram bit x to y (y can be 1 or 0)
SETLEDBYBUTTON x y = sets the led y to the button x's state
SETLEDBYRAM x y = sets the led y to the ram's bit x state
SETRAMBYLED x y = sets the ram's bit y to the led number x state.
SETRAMBYBUTTON x y = sets the ram's bit y to the button number x state.
SETBUTTONBYLED x y = sets the button y's state to the led number x's state.
JUMP x = jumps to the line you want
CONDJUMP x y z = jumps if the bit z of ram is 1 to x else to y
COPYRAM x y = copies the bit from y to x
COPYRAMBYTE x y = copies the byte (x...x+7) to byte starting from y (y...y+7)
CLEARRAMBYTE x = clear the byte starting from bit x to bit x+7
INC x = changes byte starting from bit x to bit x+7 by 1.
DEC x = same as INC, just subtracts 1.
ADD x y z = adds number x to y and saves the byte from bit number z if the result is over 255 it jumps to 0
SUB x y z = subtracts number y from x and saves the byte from bit number z  if the result is under 0 it jumps to 255
COPYRAMTOSTOR x y = replaces bit x of storage with bit y of ram
COPYSTORTORAM x y = replaces bit x of ram with bit y of storage
SETSTOR1 x = sets bit x to 1
SETSTOR0 x = sets bit x to 0
AND x y z = if bit no. x and bit no. y is on, saves 1 to bit number z, else saves a 0.
OR x y z = if bit no. x or bit no. y (or both) are on, save 1 to bit number z, else saves a 0.
XOR x y z = same as or, but when both are on, it saves a 0.
NOT x y = if bit no. x is 1, saves a 0 to bit y, else a one.
IMPLY x y z = if bit no. x is zero, it allways saves a 1 to bit z, if bit no. x is 1, and bit no. y 0, the output is zero, for one and one result is one too.
RANDOM x = gives a random value from 0 - 255 and saves it from bit x until x + 7 (total 8 bits, one byte)
RANDOMBIT x = sets bit number x to either 1 or 0 randomly
FUNC x y z = makes function x, sets its start at x and end at z.
<Function name> x y z = runs function and passes x y z, when in function you can set x y z's of the inst in the function to 'x' 'y' and 'z' to use the passed num/string from function.
RETURN x = sets return to value x, x can be anything. you can use 'return' instead of a argument (instead of x y and z) to use the value from return.
NUMTOCACHE x = saves the raw number (from bin to a number) to cache
RESETCACHE = resets cache
SETCACHE x = sets cache to x
INC x = sets byte starting from x to x+7 to the previus byte plus one
DEC x = same as INC just subtracts 1 instead
BEEP = beep for 0.10 seconds (:
```


## SYNTAX
1. Please do not use spaces infront of instructions, it will not work.
2. Please do not use comments in the same line as a instruction, it will not work. You can use the comments in its own line.
3. 'x' 'y' and 'z' used outside of functions do not work. Only 'return' and 'cache' works outside a function as a variable.
4. Its not recomended to use HALT, NOP or DELAY as for debugging.
5. Tip: use cache to store numbers temp for arguments! You can use 'cache' as a argument for inst.
6. For more info ask Simonko-912 on github to add syntax here.


