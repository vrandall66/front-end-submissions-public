## Student: David Gitlen & Chris Lane
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Great number of commits
  * Be more specific with commit messages on what you worked on
  * Also careful about branch names
* Fun bug, what happens if a user doesn't set a range?  Guessing 1 still says it's too high.
* A little too much extra space at the bottom
* Make sure there is a little more space between the header and subtitle
* When a user wins, the card should show on the top
* Reset should update clear out the latest score
* When there is an error, missing the pink border
* Little bug where outside the range isn't working just yet
* Also bug where there is no error with setting a min higher than the max
* Careful of cards spilling out if the user wins multiple times
* Should not be able to win multiple times
* Not responsive all the way down to 320px
* For future projects, try and include a noramlize/reset css file
* Careful of having so many forms, group all similar elements together under one form
  * This includes related buttons as well
* Cheers to experimenting with the output element
* Work on some heiarchy with the p tags displaying latest guesses
* Great organization of styles and alphabetizing properties within each class
* Good work grouping some styles together
* Try and stay away from percentages on margins and paddings (especially decimals)
* Good work with organization of global variables, event listeners, and function declarations
* Clean up console.logs 
* How could we refactor challengerOne and challengerTwoCompareNumbers into one function using arguments vs parameters
* Wouldn't recommend starting all of those variables out as null
  * Assign them to their querySelected elements and then grab the values in the event listeners
* Be consistent with using variables
  * Example in resetGameButton and clearChallenger forms, we are querying the guess-1-form and guess-2-form.  Let's create a variable that I can access more easily as opposed to querying it multiple times.
* enableClearButton I would use document.querySelectorAll
* Might see how you can fire error functions first...and then if there are no errors, fire the rest of the functions to update names and guesses.  As opposed to do all of them

### Functional Expectations

* __Novice:__ Application meets all of the expectations of phase one.
* __Advanced Beginner:__ Application meets all of the expectations of phase two.

------------------------------------------------------------------

### Comp Recreation

* __Advanced Beginner:__ Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.). Transitions between screen sizes may not be smooth.

------------------------------------------------------------------

### HTML - Style and Implementation

* __Advanced Beginner:__ Application adds to the above with HTML that incorporates semantic HTML elements and has a simple, clean HTML structure.

------------------------------------------------------------------

### CSS - Style and Implementation

* __Proficient:__ Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle and
  * Has 3 or less media queries for responsiveness

------------------------------------------------------------------

### JAVASCRIPT - Style and Implementation

* __Advanced Beginner:__ Displays good understanding of arguments vs parameters and:
  * Uses function declarations over anonymous functions in event listeners
  * Uses if/else statements to handle multiple paths of logic/error handling