## Student: Patrick Goulding & Matthew Kaplan 
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Great work on number of commits and detailed commit messages
    * Use the imperative tense on commits
* Be more descript with branches and create more branches
* Good attention to detail and UX
* Should have an event listener on the inputs to determine if the clear button is disabled or enabled
* A couple details with spacing of elements but in general, very good detail on UI
* Don't need the div around the main (use flex on the main); 
* A few places where we should use a form for handling our inputs and buttons
    * Also should use labels instead of p tags for things like Min Range and Max Range
* A couple places where it gets a bit nested
    * Especially in the HTML in the javascript file
    * I would also not recommend using an `article` in your card
* Remember to include box-sizing border box
* Good organization of styles and alphabetizing properties
* Nice work grouping up styles and classes together that share similar styles
    - A few places where we can continue to do this
* Good organization of global variables, event listeners, and function declarations
* Could refactor a lot of the conditionals in errorhandling functions
    * Try using the || operator
    * Can refactor emptyNameInputs and emptyGuessInput functions into one
* Instead of running all of the functions at once in playGame, run the emptyInputs functions first, then if everything is valid, we can begining to run the other functions.
    * Instead of having to check all of the things in each function, we can have one function check things first, then if things are good, move on to another part of functionality where we add the names and latest guesses.
* Do not need the else and `return` lines 225-227
* Clean up comments and console.logs before eval
* Excellent work breaking out some functions to make them dynamic like the defaultLatestScore
* Make sure you are able to describe a function even if you haven't built it
* Try and stay away from alerts
* Shouldn't need to query an element again in a callback function if it's already in a global variable
* Good use of event delegation for delete button

### Functional Expectations

* __Proficient:__ Application meets all of the expectations of phase three.

------------------------------------------------------------------

### Comp Recreation

* __Proficient:__ Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward.

------------------------------------------------------------------

### HTML - Style and Implementation

* __Novice:__ Crafts markup according to the [turing html style guide](https://github.com/turingschool-examples/html)

------------------------------------------------------------------

### CSS - Style and Implementation

* __Proficient:__ Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle and
  * Has 3 or less media queries for responsiveness

------------------------------------------------------------------

### JAVASCRIPT - Style and Implementation

* __Advanced Beginner:__ Displays good understanding of arguments vs parameters and:
  * Uses function declarations over anonymous functions in event listeners
  * Uses if/else statements to handle multiple paths of logic/error handling