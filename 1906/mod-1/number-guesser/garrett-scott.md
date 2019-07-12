## Student: Garret Iannuzzi and Scott Schipke
## Evaluator: Khalid Williams
## Notes/What To Work On:

__General__
* Github looks good
* Nice justification for keeping the update button enabled on page pageLoad
* Clear button clears out the inputs
* Cards adding tot eh

__Comp__
* No error SVGs but the errors themselves are dynamic and good looking
* Took really nice
* A little bit of overflow going on with your transitions
* A few spelling and capitalization issues on the header
* Don't forget to add in the error SVGs


__HTML__
* BEM naming conventions
* In the future, use `for` attributes on your labels
  * ARIA for attributes may be the solution here
* Found a cool place to use alt tags

__CSS__
* Good organization of stylesheet
* There seem to be a few areas where you could recombine rules, but one the whole things seems pretty good
* Stacking selectors where appropriate


__JS__
* Keeping functions pretty singly responsible for the most part, but there is some repetition in various functions
* There are a few areas where you could refactor your functions to make them less repetitive
  * Didn't get to as much refactoring as would have been ideal
  * Enable functions are a good spot for this
* Using event delegation, which is awesome
* Remove your console.logs!!! (line 112)
* Very close to proficient, but the functions get a little too repetitive for the project to be considered 'DRY'

### Functional Expectations

* Novice: Application meets all of the expectations of phase one.
* __Advanced Beginner:__ Application meets all of the expectations of phase two.
* Proficient: Application meets all of the expectations of phase three.
* Exceptional: Application adds three or more of the extensions from phase four.

------------------------------------------------------------------

### Comp Recreation

* __Novice:__ Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)
* Advanced Beginner: Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.). Transitions between screen sizes may not be smooth.
* Proficient: Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward.
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
* Advanced Beginner: Application adds organization for the whole stylesheet and within rules and
  * Has 5 or less media queries for responsiveness
* __Proficient:__ Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle and
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
