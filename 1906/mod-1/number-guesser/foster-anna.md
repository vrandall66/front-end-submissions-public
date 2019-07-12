## Student: Foster Taylor and Annie Olsen
## Evaluator:
## Notes/What To Work On:

__General__
* Good driver nav at the start of the project
* Remote workflow seemed to be good
* Have error svgs but no error messages
  * Error styling isn't quite there, no pink borders getting added to the inputs
* Make sure to get everything working in iteration 2 before getting too deep into iteration three
  * Cards are added to the page and can delete, but the errors aren't totally right
* No range displayed on page load

__Comp__
* Nice transitions for the media queries
* The error styling is missing (pink borders on inputs)
* In the future, focus on getting all parts of the base iterations done before jumping into extension-level styling


__HTML__
* good naming conventions
  * BEM  related structure
* Use `for` attributes in your labels in the future
* alt tags in the `<img>`


__CSS__
* Organized by page flow
* Properties are alphabetized
* Good job stacking selectors
* Remove empty selectors (line 96)
* Be consistent with code styling (line 123)
* Combine selectors where applicable (line 269 - 284)



__JS__
* No anonymous functions
* Handled the `e` edge case in the inputs
* Functions could be refactored to reduce codebase
  * guessingMessage functions
  * numericError message
* A few unnecessary global variables
* Can speak to areas of refactoring
* Not using event delegation
  * This is the main thing holding you from proficient (that and refactoring)
* Make event delegation a big focus over the weekend
* Always leave time to DRY up functions throughout development. It's the most common thing that leads to advanced beginner in JS

### Functional Expectations

* Novice: Application meets all of the expectations of phase one.
* __Advanced Beginner:__ Application meets all of the expectations of phase two.
* Proficient: Application meets all of the expectations of phase three.
* Exceptional: Application adds three or more of the extensions from phase four.

------------------------------------------------------------------

### Comp Recreation

* Novice: Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)
* Advanced Beginner: Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.). Transitions between screen sizes may not be smooth.
* __Proficient:__ Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward.
* Exceptional: Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements that have been added match the visuals established in the comps.

------------------------------------------------------------------

### HTML - Style and Implementation

* Novice: Crafts markup according to the [turing html style guide](https://github.com/turingschool-examples/html)
* Advanced Beginner: Application adds to the above with HTML that incorporates semantic HTML elements and has a simple, clean HTML structure.
* __Proficient:__ Application adds to the above with markup that is easy to read and follows across naming conventions
* Exceptional: Application adds to the above by using [BEM](http://getbem.com/), [SMACCS](https://smacss.com/), or another set of naming conventions for classes and:
    * Implements html that is accessible for folks with visual disabilities. Reference [this lesson plan](http://frontend.turing.io/lessons/floating/web-accessibility.html)

------------------------------------------------------------------

### CSS - Style and Implementation

* Novice: Crafts CSS according to the [turing css style guide](https://github.com/turingschool-examples/css)
* __Advanced Beginner:__ Application adds organization for the whole stylesheet and within rules and
  * Has 5 or less media queries for responsiveness
* Proficient: Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle and
  * Has 3 or less media queries for responsiveness
* Exceptional: Application adds to the above by using [BEM](http://getbem.com/), [SMACCS](https://smacss.com/), or another set of naming conventions for classes

------------------------------------------------------------------

### JAVASCRIPT - Style and Implementation

* Novice: Crafts JS according to the [turing js style guide](https://github.com/turingschool-examples/javascript/tree/master/es5)
* __Advanced Beginner:__ Displays good understanding of arguments vs parameters and:
  * Uses function declarations over anonymous functions in event listeners
  * Uses if/else statements to handle multiple paths of logic/error handling
* Proficient: Application uses event delegation correctly on dynamic elements and:
  * Keeps functions DRY with a focus on SRP and can call functions within functions
  * There are no nested if/else statements
*  Exceptional: Functions and code are well-refactored and show developer empathy and:
  * No global variables aside from query selectors, min & max, number of guesses, and start time
  * All functions are less than 10 lines
  * Uses logical operators instead of if/else statements where applicable
