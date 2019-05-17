## Student: Greg Anderson & Edward Cheatham
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Make sure to keep an eye on number of commits for future projects to make sure both sides are even
* Some issues with errors not working
* Some bugs where submissions weren't working
* Some issues with things getting knocked out of space on mobile view
* Careful of inline styles in your HTML
* Gets a bit div happy in the form for the challengers
* Make sure tabbing is correct as well
* Too many divs and spans in the HTML template literal (make sure the dynamic cards are semantic and tabbed in correctly as well)
* Would have both challengers all in one form as opposed to two
* Good approach to organizing styles, but make sure there is organization to the properties in each selector!
* Remember not use to `flex` on your body!
* Some places where we can group styles more often.
  * Such as card__article--winer and card__section
* Currently missing media queries
* Good organization of global variables, event listeners, and function declarations
* Good use of arguments vs parameters with making checkResults and making that function dynamic
* Some good examples of calling functions inside of other functions and using operators for variable assignments
* Great work using event delegation for deleting functionality
* See how you could refactor validateForAlphaNumberic and validateForNumeric into one
* Stay away from double assignment operators in the increasedRange function
* What is the purpose of returning values?  If it's not being stored anywhere, you don't need the return
  * guessCounter, generateRandomNumber
  * whoWin() is a good example where the return is necessary
* Likely don't need one line functions like resetCounter if it's not being used anywhere else.
* Try and stay away from inline styles
* As opposed to firing all functions at once like keyPressPlayerFormEvent, try firing only the functions you need in the beginning, and then based on a conditional, fire the next function.

### Functional Expectations

* __Novice:__ Application meets all of the expectations of phase one.

------------------------------------------------------------------

### Comp Recreation

* __Novice:__ Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)

------------------------------------------------------------------

### HTML - Style and Implementation

* __Novice:__ Crafts markup according to the [turing html style guide](https://github.com/turingschool-examples/html)

------------------------------------------------------------------

### CSS - Style and Implementation

* __Novice:__ Crafts CSS according to the [turing css style guide](https://github.com/turingschool-examples/css)

------------------------------------------------------------------

### JAVASCRIPT - Style and Implementation

* __Proficient:__ Application uses event delegation correctly on dynamic elements and:
  * Keeps functions DRY with a focus on SRP and can call functions within functions
  * There are no nested if/else statements