## Student: Ann Cerveny & Katie Williams & Jev Forsberg
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Great number of commits but make sure to be consistent with commit messages
* Be consistent with branch names using kabob case and being specific
* Would also recommend more branches
* Great work on your README
* Missing the search ui button and might put a little padding in the inputs
* Color of `Filter Starred Ideas` and `New Quality` is off a little bit
* Spacing of the delete button to the edge of the card is a little off from the comp. 
  * Notice it is uneven compared to the star and the end of the card as the window gets bigger.
* Continue to keep working on keeping the star staying updated
* Not responsive on mobile layouts
* Really clean structure and nice use of BEM classes within the HTML
* Remember to include a normalize or reset css stylesheet
* Might have each of the qualities in a nav within a form
  * I think since they are related, the input and button to add a new quality could also be in the same form
* Remember to include box-sizing border box
* Good organization of styles and alphbetizing properties
* Might experiment with short hand versions of margin like in lines 69 - 71
* I would recommend not including the quality array in each class and then the quality property only keeping track of an index, instead of still giving it a value of the string (easier to increment/decrement with a number)
* See how you can refactor updateTitle, updateBody, and updateStart so that they use bracket notation (this might also help clean up your editCardBody in the main.js)
* Good organization of global variables, event listeners, and function declarations
* See how you can only have one event listener on the cardTable listening for the click to handle the deleteDisplayedCards and editStars
* How could we refactor the enableSaveButton where we store the value of the expression, and then assign the variable to the disabled property
* Remember to stay semantic with your HTML for each card that gets appended.  I think the entire `card` could be more specific than a div.
* Good use of event delegation and the closest method
* Good use of array prototype methods like findIndex, forEach, and map
* Continue to experiment using toggleClass for the star
* See how you can refactor the enterToBlur function so you don't have to use the same conditional twice.  `hint: e.target.blur()`

### Functional Expectations

*  Novice: Application meets all of the expectations of phase one.

### Comp Recreation

*  Novice - Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)

### HTML - Style and Implementation

*  Proficient - Applications adds to the above with markup that is easy to read and follow across naming conventions

### CSS - Style and Implementation

*  Exceptional - Application adds to the above by using BEM, SMACCS, or another set of naming conventions for classes

### JAVASCRIPT - Style and Implementation

*  Proficient - Application adds readability by incorporating both DRY and SRP practices and students can speak to implementation decisions and:
  *  Uses event delegation correctly on dynamic elements for deleting, editing, & starring an idea
  *  All functions are less than 10 lines
  *  There are no global variables aside from query selectors and two arrays for your ideas and qualities
  *  There are no nested if else statements