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
Work-In-Progress.  Essentially playable on a single-puzzle, with basic "you win" detection but no "you lose" implemented yet

# DONE
* Tile bitmaps .  NOW IN THE CORRECT ORDER (including the 'remaining tiles' panel)
* Cursor movement (auto-repeat, locking (now including locking to sliders), impassable blocks).
* Falling
* Match detection
* Destruction animation
* Clock ticking (animation plays concurrently i.e. clock doesn't halt, unlike ZX Spectrum version)
* Ascii/numeric font (8x8) - including drop-shadow effect!
* Puzzle data for two more more puzzles. (But definitely incomplete)
* Scoring including bonus calculation
* bonus icon/animation  (an icon that shows 400, 600, 1000 to 2000 appears over the playing field when you get a bonus - with masking)
* bonus icon/animation now using 1-pixel vertical scrolling
* bonus icon/animation now using colourizing bonus bitmaps!
* sfx
* Vertical sliders (90% complete) although still some bugs with pushing blocks onto/off existing stacks
* "Clear" (you win) condition when all tiles have been matched
* "next level" after win condition
* Clock font - nice shiny fat 16x16 bitmaps! Several colours (yellow, red, green), as required.
* "Panic Mode" clock implemented - clock color changes at 30s or less remaining, and flashing at 10s or less remaining
* Information (which puzzle you're on, "Player 1"). Implemented the multiple nested level numbers e.g. "Level 5 [1-3]"
* Shiny glint of light on tiles, which occurs randomly during play


# TODO
*  "time over" (lose) condition
*  end of level scoring (clear bonus, time remaining, tick tick tick kerching!)
*  Horizontal sliders.. very important and lots of work.
*  This requires one-pixel-shifted versions of all tiles
*  both variants of wall tiles in both blocking and non-blocking versions (i.e. one kind cursor cannot pass, one kind cursor can pass)
*  'background' bricks and anything else surrounding the play area (50% done)
*  level select between stages / initial level select at start
*  retry (i.e. abort, start again) and count of remaining retries
*  high score table
*  music (50% done)
*  attract screen / demo mode
*  intro screen
*  two player mode
*  diagonal cursor movement not yet done.
*  joystick not yet done (50% done)
*  minimize redrawing things that haven't changed - in particular re-rendering all the clock digits if only one clock digit has changed (but would only be a small optimization, since the flashing "panic mode" clock needs to be fully redrawn every 4th frame anyway)

# TODO LATER
*  Passwords for level skip
*  Gravnic mode
*  Arcade mode
*  In-game backgrounds and pretty pictures?

# To build
I use VSCode with pyz80 extension: https://marketplace.visualstudio.com/items?itemName=simonowen.pyz80
Using the default settings, you can launch SimCoupe by opening first.z80 in VSCode and pressing Ctrl+F10 

# Thanks
* Simon Owen
* Stefan Drissen
* Dan Dooré
* Balor Price


![image](https://user-images.githubusercontent.com/4968348/111890000-75ad4700-89dd-11eb-8756-2f983a51744f.png)

