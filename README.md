# jQuery

This repo will be used for web development jQuery in class demo and exercise


## Simon Dice Challenge

**1. Add Javascript and jQuery:**
    - Our game logic will be created inside an external Javascript file.
    - Create a new file called game.js
    - Link to this new external JS file from your index.html
    
**2. Create a new Pattern:**
    - Inside game.js create a new function called nextSequence()
    - Inside the new function generate a new random number between 0 and 3, and store it in a variable called randomNumber
    - At the top of the game.js file, create a new array called buttonColours and set it to hold the sequence "red", "blue", "green", "yellow" .
    - Create a new variable called randomChosenColour and use the randomNumber from step 2 to select a random color from the buttonColours array.
    - At the top of the game.js file, create a new empty array called gamePattern.
    - Add the new randomChosenColour generated in step 4 to the end of the gamePattern.
    
**3. Show the Sequence to the User with Animations and Sounds:**
    - Use jQuery to select the button with the same id as the randomChosenColour
    - Use jQuery to animate a flash to the buttonattern adding a `.fadeIn(100).fadeOut(100).fadeIn(100);` effect.
    - Create a functoin called `playSound` that receives the random chosen color as argument.
    - Inside the `playSound` function create the object audio using the color name and play it.

**4. Check Which Button is Pressed:**
    - Use jQuery to detect when any of the buttons are clicked and trigger a handler function `$(document).keypress(function()`.
    - Inside the handler, create a new variable called userChosenColour to store the id of the button that got clicked using `$(document).keypress(function()`. 
    - At the top of the game.js file, create a new empty array with the name userClickedPattern.
    - Add the contents of the variable userChosenColour created in step 2 to the end of this new userClickedPattern

**5. Add sounds and animations to buttom clicks:**
    - Use the previously created `playSound()` function that takes the  input parameter called `userChosenColour`.
    - Create a new function called `animatePress()`, it should take a single input parameter called `currentColour`.
    - Take a look inside the styles.css file, you can see there is a class called `"pressed"`, it will add a box shadow and changes the background colour to grey. 
    - Use jQuery to add this pressed class to the button that gets clicked inside `animatePress()`.
    - Add a timeout to remove the class pressed


**6. Start the game:**
    - Use jQuery to detect when a keyboard key has been pressed, when that happens for the first time, call `nextSequence()` use event listener `keypress()` in document.
    - You'll need a way to keep track of whether if the game has started or not, so you only call nextSequence() on the first keypress.
    - Create a new variable called level and start at level 0. 
    - The h1 title starts out saying "Press A Key to Start", when the game has started, change this to say "Level 0" i `nextSequence()`.
    - Inside nextSequence(), increase the level by 1 every time nextSequence() is called.
    - Inside nextSequence(), update the h1 with this change in the value of level.


