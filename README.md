# SamPuzznic
Sam Coupé Puzznic clone, written in 100% z80 assembler.
The Sam Coupé is an utterly obsolete 8-bit microcomputer, from the 1980s (just about - it was released in 1989).  I happened to own one (and subsequently sold to a collector 20 years ago).
These days, emulators such as SimCoupe provide faithful recreations of this weird machine.
Puzznic is a video game (arcade, home computer and console ports) from Taito, released also in 1989.
Despite Puzznic being released on most of the contemporary home computer systems, it was never released for the Sam Coupé.
This was NOT NECESSARILY a contributing factor in the demise of the machine.


# Background
I started making 'my own Puzznic' in around 1993/4/5, when I was a teenager, making some tiles and graphics,
and a couple of 'short examples' of gameplay behaviour in Sam Basic.
I recently rediscovered the original floppy disks with that work, and decided to see
if I could implement the full game from scratch.
I've never really finished any z80 projects.  I have a lot of started-some-ideas-and-then-stopped,
mostly because I didn't have the requisite skills back then. This is the first 'recent' z80 thing
I've done.

# Status
Work-In-Progress.
Tiles graphics imported, lots of other graphics missing.
Most of the movement/falling logic is in place, including the matching routine, which can find single and multiple
matches triggered by falls.  Matched tiles currently just 'disappear immediately' without fanfare, but this correctly
triggers another fall of any tiles above the matched ones.
No sliders/elevators yet.
No level select, scoring, bonus-multiplier graphics, game-over, etc.

# To build
I use VSCode with pyz80 extension: https://marketplace.visualstudio.com/items?itemName=simonowen.pyz80
Using the default settings, you can launch SimCoupe by opening first.z80 in VSCode and pressing Ctrl+F10 

# Thanks
* Simon Owen
* Stefan Drissen
* Dan Dooré
* Balor Price


![screenshot](https://user-images.githubusercontent.com/4968348/110262177-bc954880-7faa-11eb-9763-006418b0b2d1.png)
