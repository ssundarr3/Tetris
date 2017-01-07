![tetrispic1](https://cloud.githubusercontent.com/assets/16379542/21737898/b51e0d62-d44b-11e6-91e9-17f2b4ca196a.jpg)

![tetrispic2](https://cloud.githubusercontent.com/assets/16379542/21737919/0077fb74-d44c-11e6-80f5-419e87d7e05b.jpg)


NOTE: This repo will only contain the executable due to University Policy. 
For the code, e-mail me at: ShridharSundarraj3@gmail.com

Quadris (Latinization of Tetris) 
CS 246 Fall 2016 
Project Members: Shridhar Sundarraj, Ian Lai, Jonathan Litovitz

To Compile, go to Quadris/final/ and make
./quadris to run


Commands: (Note: These commands are auto-completed. i.e. lef = left, but level is ambiguous as it can be levelup/down)
--------- (Note: You can use multipliers with these commands. i.e. 4lef moves 4left.)

left
right
down
drop

clockwise
counterclockwise

levelup
leveldown

norandom file: Relevant only during levels 3 and 4, this command makes these levels non-
random, instead taking input from the sequence file, starting from the beginning. This is
to facilitate testing
random: Relevant only during levels 3 and 4, this command restores randomness in these levels.

sequence file: Executes the sequence of commands found in file. This is to facilitate the
construction of test cases.

I, J, L, etc.: Useful during testing, these commands replace the current undropped block with
the stated block. Heaviness is detemined by the level number. Note that, for heavy blocks,
these commands do not cause a downward move.

restart

Command Line Interface:
-----------------------

-text: runs the program with text only
-seed xxx: sets the random number generator’s seed to xxx. If you don’t set the seed, you
always get the same random sequence every time you run the program. It’s good for testing,
but not much fun.
-scriptfile xxx: Uses xxx instead of sequence.txt as a source of blocks for level 0
-startlevel n: Starts the game in level n. The game starts in level 0 if this option is not
supplied.


LEVELS
------

Level 0: Takes its blocks in sequence
from the file sequence.txt (a sample is provided), or from another file, whose name is
supplied on the command line. This level is non-random, and can be used to test with a
predetermined set of blocks. Make sure that sequence.txt, and any other sequence
files you intend to use with your project, are submitted to Marmoset along with
your code.
• Level 1: The block selector will randomly choose a block with probabilities skewed such that
S and Z blocks are selected with probability 1
12 each, and the other blocks are selected with
probability 1
6
each.
• Level 2: All blocks are selected with equal probability.
• Level 3: The block selector will randomly choose a block with probabilities skewed such that
S and Z blocks are selected with probability 2
9
each, and the other blocks are selected with
probability 1
9
each. Moreover, blocks generated in level 3 are “heavy”: every command to
move or rotate the block will be followed immediately and automatically by a downward move
of one row (if possible).
• Level 4: In addition to the rules of Level 3, in Level 4 there is an external constructive force:
every time you place 5 (and also 10, 15, etc.) blocks without clearing at least one row, a
1x1 block (indicated by * in text, and by the colour brown in graphics) is dropped onto your
game board in the centre column. Once dropped, it acts like any other block: if it completes
a row, the row disappears. So if you do not act quickly, these blocks will work to eventually
split your screen in two, making the game difficult to play

Scoring
The game is scored as follows: when a line (or multiple lines) is cleared, you score points equal to
(your current level, plus number of lines) squared. (For example, clearing a line in level 2 is worth 9
points.) In addition, when a block is completely removed from the screen (i.e., when all of its cells
have disappeared) you score points equal to the level you were in when the block was generated,
plus one, squared. (For ex



EXTRA FEATURES:
---------------
1.Macro Language: Enable feature by adding flag: -extraFeatureMacro.
Usage: Macro MacroName command1 command2 .... -1. Calling MacroName is
equivalent to calling command1 command2 ... individually. The MacroName can
be called with the least ambiguous name similar to other commands and with
multipliers.

2. Variable Grid Size. Enable feature by adding flag: 
-extraFeatureGrid numRows numCols 


