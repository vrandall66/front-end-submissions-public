## Student: Dylan Hofmann, Karin Ohman, & Gabriel Inzurriaga
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Really nice work creating lots of commits
  * Continue to keep working on more detailed commits (what specifically did you refactor)
  * Nice work with creating more branches.  Continue to make more branches, but nice improvement.
* Really clean and effective UI
  * I would make sure that the letters wrap around when typing long messages
  * Make sure that the cards come back in the correct order when clicking show more, less, all, etc.
* Might add a bit more spacing between buttons and cards on mobile view
* Use spans only when you need to.  For example, h1, style it one way and then use a span to style one word differently 
  * I would keep similar/related inputs in one form and then a couple divs to style things
  * Keep classes for styling purposes, and for javascript use ids so you can grab that element
* Nice work with organization of styles and alphabetizing properties
  * For BEMS or SMACCS, look into formatting of names of styles (if SMACCS, divide things into layers like class `l-card-section`)
  * Some good areas where you are grouping styles.  A few more sections where classes that have similar widths or flex properties that could be grouped together as well
* I would suggest making the array of qualities locally scoped instead of global since it is static and does not need to change
* Nice work with filtering
  * When trying to add the display none, use classes instead of inline styles
  * I would challenge you to remove elements from the DOM instead of doing display none
* Nice work using array prototypes over for loops
* Nice work creating functions that you can reuse
* Cheers on jumping into using arrow functions and exploring some es6
* Some really creative ways of reducing code, like using a forEach on the inputs and adding similar event listeners

### Functional Expectations

*  Exceptional - Application adds all of the extensions

### Comp Recreation

*  Exceptional - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements that have been added match the visuals established in the comps

### HTML - Style and Implementation

*  Proficient - Applications adds to the above with markup that is easy to read and follow across naming conventions

### CSS - Style and Implementation

*  Proficient - Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle

### JAVASCRIPT - Style and Implementation

*  Proficient - Application adds readability by incorporating both DRY and SRP practices and students can speak to implementation decisions and:
  *  All functions are less than 10 lines
  *  There are less than 3 global variables
  *  There are no nested if else statements