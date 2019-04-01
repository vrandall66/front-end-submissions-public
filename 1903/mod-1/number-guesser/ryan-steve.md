## Student: Ryan Flachman & Steve Rumizen
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Good number of commits and being consistent with commit messages
* Keep branch names consistent and clear/ could have more branches
* Include images of your project in the README
* Make sure the height takes up the full height
* Couple bugs with errors like if I guess a number over the range
* Current range should only increase/decrease by 10 after winning a game
* X in delete button isn't quite centered
* Nice work with the Konami code
* Inputs get a little close as the screen squishes
    * On tablet view, I'd see how you can still take up the full space
    * Good attention to the table view, I'd see how I can make the transition a bit smoother
* Good work reusing classes and using forms for each element
    * Would keep challenger 1 and 2 inside of one form
    * Clean up the spans and put them on the initial html tags
* Might cut back a little bit on the divs on the card and have some heirarchy instead of all the p tags in it
* Remember to include box-sizing border box
* Keep text-align: center only on text elements
* Great organization and alphabetizing properties
    * Be consistent with using rules (if you're using the short hand of margin)
    * A few areas where styles can be grouped together, but in general, good work on this
* Good organization of variables, event listeners, and function declarations
    * Would use function declarations instead of anonymous functions in the event listeners
* numberCheck could be refactored into one function instead of running conditionals twice
  * Could do something similar with the updateErrors function, creating a separate function that you can call to update the styles and pass an argument depending on which input we're updating
* Good use of bracket notation for the konami code
* Think about how you can refactor some of these game functionality into its own class
    * A class for the settings for the game
* Careful of using inline styles, might see how you can use classes or the toggleClass method
* In your event listeners, see how you can run functions based on conditionals instead of running all of them at once
    * If there are no errors, then generate the number, etc.



### Functional Expectations

* __Exceptional:__ Application adds three or more of the extensions from phase four.

------------------------------------------------------------------

### Comp Recreation

* __Proficient:__ Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward.

------------------------------------------------------------------

### HTML - Style and Implementation

* __Advanced Beginner:__ Application adds to the above with HTML that incorporates semantic HTML elements and has a simple, clean HTML structure.

------------------------------------------------------------------

### CSS - Style and Implementation

* __Proficient:__ Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle and
  * Has 3 or less media queries for responsiveness

------------------------------------------------------------------

### JAVASCRIPT - Style and Implementation

* __Proficient:__ Application uses event delegation correctly on dynamic elements and:
  * Keeps functions DRY with a focus on SRP and can call functions within functions
  * There are no nested if/else statements