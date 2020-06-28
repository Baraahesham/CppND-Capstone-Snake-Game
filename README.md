# CPPND: Capstone Snake Game Example

This is a starter repo for the Capstone project in the [Udacity C++ Nanodegree Program](https://www.udacity.com/course/c-plus-plus-nanodegree--nd213). The code for this repo was inspired by [this](https://codereview.stackexchange.com/questions/212296/snake-game-in-c-with-sdl) excellent StackOverflow post and set of responses.

<img src="snake_game.gif"/>
-----------------------------

## Project Describtion:
This project is an extension of the snake game demo I have extended the game with barriers added to the game. There are two types of barriers, fixed barriers location that is  parsed from "Barrier" file and other random barriers instantiated randomly on each run.
--------------------------------

## File and CLass Structure:
The src folder containing the game files .The game mainly consists of 4 main classes  Controller ,game, renderer and snake.
Controlller : this class mainly responsible for handling user input on each keyboard strike.
Snake :Handling snake body,snkae head and indicating if the snake is still alive or not.
renderer: Handling rendering the game logic (i.e visualizing food,barriers,snake body.....);
game: contain mainly the Game logic and the run function which starts the game.
main function starts the game by calling the run function from class game which run infinitely by calling the following sequence :
1-controller.HandleInput()->to check for new input 
2-update()->update game logic (ie food )
3-render()->update the window according to the new inputs and logic 

Note:updatebarriers() function is called at the beginning of the update function before the loop as we dont want to render barriers on each run cause its fixed through the game.


## Addressed Rupric points :
1-The project demonstrates an understanding of C++ functions and control structures.

2-The project reads data from a file and process the data, or the program writes data to a file.
-Game class ->PLaceBarriers function.

3-The project accepts input from a user as part of the necessary operation of the program.
- Controller class handeling input from user;

4-The project code is organized into classes with class attributes to hold the data, and class methods to perform tasks.
-this demonstrated  throughout the whole project (ie project classes and objects)

5-All class data members are explicitly specified as public, protected, or private.
this demonstrated  throughout the whole project (snake class)

6-All class members that are set to argument values are initialized through member initialization lists.
 -Renderer class constructor (Renderer::Renderer())

7-Appropriate data and functions are grouped into classes. Member data that is subject to an invariant is hidden from the user. State is accessed via member functions.
 -this demonstrated  throughout the whole project


## Dependencies for Running Locally
* cmake >= 3.7
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* SDL2 >= 2.0
  * All installation instructions can be found [here](https://wiki.libsdl.org/Installation)
  * Note that for Linux, an `apt` or `apt-get` installation is preferred to building from source.
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory in the top level directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./SnakeGame`.