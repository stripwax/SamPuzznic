These are the 'raw' resources used to create the binary inclusion files.
The pipeline is somewhat manual due to laziness. Bits of the pipeline are based on original work done by me in around 1991 (?) so forgive its simplicity.

For the tiles and various game objects/fonts/etc:

1. run simcoupe with newpuzz_2.mgt disk
2. load "tile_extr3" basic program and run it (this will create the binary files IN THE DISK IMAGE)
3. save the disk image in simcoupe
4. on your build machine, use samfile to extract the .b files from the disk image e.g.

samfile-windows-amd64.exe cat -i resources\newpuzz_2.mgt -f tiles.b > tiles.b
samfile-windows-amd64.exe cat -i resources\newpuzz_2.mgt -f alpha.b > alpha.b
samfile-windows-amd64.exe cat -i resources\newpuzz_2.mgt -f alpha2.b > alpha2.b
samfile-windows-amd64.exe cat -i resources\newpuzz_2.mgt -f bonus.b > bonus.b
samfile-windows-amd64.exe cat -i resources\newpuzz_2.mgt -f fatnums.b > fatnums.b  
samfile-windows-amd64.exe cat -i resources\newpuzz_2.mgt -f glint.b > glint.b 
samfile-windows-amd64.exe cat -i resources\newpuzz_2.mgt -f bricks.b > bricks.b 

TODO: how to extract/compile the music files

TODO: background images?


Utilities
=========

Samfile: https://github.com/petemoore/samfile
