java cIntroduction to Systems Programming . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
Assignment 2
Accompanying this assignment you will ffnd an archive ffle gt2048.zip. The zip contains a directory gt2048,
with a BlueJ Java project for the GT 2048 application.
2048 is a puzzle game implemented originally as a web-based video game in 2014. The game has a 4 × 4 grid
sliding board with numbered tiles, where tiles get combined according to user moves. The goal of the game is
to combine tiles so as to reach a board conffguration containing a tile with value 2048.
Initially, the board starts with only two tiles, placed in random positions, and containing each either 2 or 4. The
user interacts with the game by moving in four possible directions (up, down, left or right). The user movement
causes the tiles to move as far as possible in the chosen direction, until reaching another tile, or the edge of the
board. When two tiles of the same number collide while moving, they will merge into a tile whose value is the
sum of the two colliding tiles. After each movement, and only if the board has changed its conffguration as a
consequence of the move, a new tile is randomly located at a free slot in the board, with either 2 or 4 (randomly
chosen). When a board with no free slots where to place the spawning tile is reached, the game ends. There are
some subtleties in the game playing too, such as a “merged tile” not being able to be combined with another
tile in the same movement, as well as in the order in which the merging occurs (tiles closer to the edge of the
board limiting the movement merge ffrst).
Project GT2048 is a text-based implementation of the 2048 game. It consists of four classes:
• GT2048Cell: it is the simplest of the classes. It models a cell of the 2048 board, with all its possible
states: “empty”, or containing a numeric value. The value of a non-empty cell must be a power of two,
due to the rules of the game. This class is accompanied by a test suite, i.e., a class containing unit tests
for some of the methods of the GT2048Cell class.
• GT2048Board: it models the board through a bi-dimensional array of cells, each cell being represented by
a GT2048Cell object. It contains methods to initialize the game, react to user movements, etc.
• GT2048InputReader: it implements the reading of input commands.
• GT2048: the main class of the game. Its constructor creates the input reader object and game board, and
enables initiating the game by calling method startGame().
Your assignment consists of various tasks:
1. Study the behavior of the game by interacting with it in https://play2048.co.
2. Study the provided implementation (including the provided tests), so as to understand how the solution
is organized and partially implemented.
3. Implement all the methods with missing implementations in class GT2048Board. These include all the
methods that implement movements, as well as the ones that decide whether a given movement is possible.
4. Create a test class for testing GT2048Board. Design and implement in the test class sufffcient unit tests
to thoroughly check the c代 写program、Java
代做程序编程语言orrect behavior of at least one movement method. Try to cover with your tests
all the statements in the selected method (i.e., every statement in the method should be executed by at
least one test).
5. If you ffnd errors (bugs) in the existing code (not your implementation, but the existing code), you must
ffx them and provide unit tests that fail for the original buggy code, and pass with your ffx. Your unit
tests should describe, in the comment, what the found bug was, and how was solved.6. The previous tasks should lead you to a fully functional implementation of the game. Identify at least
one design problem in the implementation (e.g., tight coupling, low cohesion, duplicate code). Textually
describe the problem, and a potential solution, at the bottom of the README ffle in the project.
7. Make a copy of your solution to all tasks, and bundle it in a zip ffle, as version 1.zip, before continuing
with the following tasks.
8. Extend your implementation with behavior that implements user login, and scores. Your implementation
must not modify neither GT2048Cell nor GT2048Board (i.e., these classes should be exactly the same that
you bundled into version 1.zip. Your extension must implement the following behavior:
• Ask the user to provide its username (no password) before starting the game.
• Maintain, for each user, its corresponding highest score. The score of a ffnished game play is the sum
of all the cells in the board; it is computed only for ffnished games (either reaching 2048 or not). For
each user, we only maintain his/her highest score. When a user plays the game for the ffrst time, its
score is created with zero at the start of the game; it is updated when the player ffnishes the game.
• The application must allow players to play subsequent games without exiting, possibly changing the
user for each game play. When no game is being played, the application must allow one to print out
the scores of all players.
To implement the above score related functionality, you may modify existing classes (except GT2048Cell
and GT2048Board), and add new classes. Your solution must not implement any persistence mechanism,
i.e., when the application is terminated, all scores are lost.
Your assignment is to fulffll all the above tasks. You may decide to add auxiliary methods as private, or
implement the required functionalities within the provided method bodies. For the ffrst part (until “version 1”
of your game), you are not allowed to change the APIs of the classes, i.e., not change method names, number
of parameters or their types.
You must submit the solution through moodle, as a zip archive containing the whole ffnal project, as well as
the version 1 project, either in a separate zip, or as a zip inside the main submission archive. This assignment
must be solved individually. The correctness of your solution is important, as so is the quality of the code
(clarity, readability, structure, etc.). The quality of your design for the score functionality, including how the
implementation is organized and how you decide to represent the necessary information (what data structures
to use), will be important.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
