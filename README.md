# Ridge Racer Revolution Unlocked
A ROM hack tool that allows you to modify an EUR or US copy of Ridge Racer Revolution directly in the browser - no downloads or uploads required.

Features (all of which are optional):
* Enable two hidden courses from the original Ridge Racer: "Seaside Route 765" and "Ridge City Highway".

* Unlock all courses in the "Extra" (reversed) variants.

* Unlock all 15 cars in the game, including the 13th devil, 13th kid and White angel.

* Unlock all four car speed levels for every course and game mode.

* Unlock the ability to select race scene / time of day.

* Disable the race time limits (makes it possible to complete the extra courses on the lowest speed level).

[Go here to patch your CD image](https://s0rent.github.io/rrr-unlocked/)

### Requirements
An uncompressed CD image with the EUR or US version of Ridge Racer Revolution.

### Disclaimer
I have not tested every combination of game modes, courses and cars, so there might be bugs somewhere that I did not encounter. However, everything that I have tried in the game has worked without flaws. I aimed for the least invasive way to perform the modifications without having to distribute a copy of the game. As a result, the logic that chooses the rival car model for the original (and otherwise inaccessible) Ridge Racer courses had to be changed to prevent a crash - it plays all the same though.

### Background info
After having owned this game for nearly 30 years, I discovered that the two courses from the original Ridge Racer game were on the CD, even though they were not accessible in the game. It was a good opportunity to try out MIPS disassembly and PS1 debugging, in order to find a way to make them accessible. Luckily, Ridge Racer Revolution is a rather early PS1 game, so it does not dynamically load/unload game code like many later games, which made it very easy to disassemble and analyse. Further more, the compiler which was used inserted NOP instructions after every branch instruction (a simple solution to account for the MIPS pipeline architecture), which meant that there were several "empty" spots for me to place the extra code required for the modifications. The choice of distributing this tool as HTML/JavaScript stems from the fact that everyone has access to a browser, no matter which platform they are on and their technical proficiency level - it requires no downloads, sketchy executables, geeky runtime envorinments, and so forth.
