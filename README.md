# NAME: Linnea P. Castro
# COURSE: CSE 224
# DATE: 31 OCT 2022
# ASSIGNMENT: PA3
# SYNOPSIS:

# This bash script creates a stick picking game. The user has the option to customize the starting number of sticks as a 
# command line argument, as long as their entry is >= 5 sticks.  If the command line is left empty, the script will
# prompt the user to enter a number of sticks and use that number for gameplay, provided it is >= 5 sticks. This script
# utilizes two functions, the first being a stick printing function.  The stick printing function takes the value
# stored in the stick variable and prints that many "|" pipe sticks. This goal is achieved using a while loop and the
# variable i, initialized to 0 and set to increment through each loop iteration as long as i is less than $sticks,
# effectively creating one "|" stick for each stick remaining in play.  This function is called after each turn, following
# stick calculation (subtracting pick from number of sticks remaining).

# The second function, called "stick picking function" is used by the computer to select number of sticks to draw.  It
# is only called at the beginning of the computer's turn.  It uses the algorithm sticks%5 to select number of sticks to
# draw.  If there is no remainder, the computer will draw 1 stick, otherwise, it will draw the remainder.  This effect
# is achieved with an if/else conditional.

# After establishing the number of sticks to play with, the gameplay loop begins with an infinite while loop.  The computer
# takes its turn first.  The computer's turn consists of calling the stick picking function, calculating remaining sticks, 
# printing remaining sticks with the stick printing function, and then checking for a win (were the last sticks drawn 
# on this turn?).  After determining there are still sticks in play, the user takes their turn.  The user is prompted to 
# choose a number of sticks to remove (1,2,3, or 4).  An infinite loop ensures the user will keep being asked for a 
# legitimate stick choice if their input is not 1-4. A legitimate entry is the ticket out of the loop, as flag changes to 0.
# The user's turn also concludes with calculating remaining sticks, calling the stick printing function, and checking for a win.  
# A win will exit the game.  Remaining sticks will loop back up to the top of the gameplay loop for the computer's turn,
# and continue to loop until the last sticks are drawn, wherein a winner will be declared and the game will exit. 

