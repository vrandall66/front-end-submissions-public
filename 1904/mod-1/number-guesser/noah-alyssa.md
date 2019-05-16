## Student: Noah Gibson & Alyssa Lundgren
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Great number of work and being consistent with clear commit messages.
  * Also good work on consistency with branches.
* Jumps just a little bit when errors come in because name disappears
* Great error handling.
* Update button gets knocked down just a bit
  * As well as some of the buttons
* A few issues with spacing and centering elements as the screen gets smaller
* Remember to include the meta viewport tag in the head for mobile views
* A few too many nested divs
* Cheers to using alt tags on images for accessibility reasons.  Shouldn't need alt tags on buttons.
* Remember to include the for attribute in lables to sync them up and make it a bit more accessible
* Great organziation of styles from top to bottom and alphabetizing properties within each class
* Good start to grouping up styles, see if you can find more instances or repeated styles you don't need
  * Examples include player-input & button-trio or input-name and input-guess 
  * When it becomes 3 or more classes, see if you can use one class and put it on multiple elements
* Careful of using position absolute and negative margins to style things (can be a little hacky)
* Great work organizing global variables, event listeners, and function declarations
* Instead of firing all of the functions in submitEverything, maybe fire the functions for errors first, and then if there are no errors, fire the functions to update guesses
* How could we refactor playerOneErrors and playerTwoErrors into one function and pass arguments through.
* Try and avoid inline styles for specificity and organization reason
* In updateAllNames, see how you can use one for loop instead of two to update the names

### Functional Expectations

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