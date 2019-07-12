## Student: Colin Koga & Victor Abraham
## Evaluator: Khalid Williams
## Notes/What To Work On:

__General__
* Github looks good on the whole

* Good split of remote and driver navigator working
* Got errors adding to the page, error borders don't disappear though
  * Error text is a little small
  * Might be a moment to use vh, em or rem instead of px
* Despite having error messages when we submit without a name, the cards can append
* Have a little stray margin on the button causing issues on page load
* The clear and reset buttons are a little buggy
  * reset button seems to be working, I thin you lost a preventDefault on the clearButton

__Comp__
* Delete button on the card is a little bigger
* Have some more stray margin causing alignment issues on the first media queries
* Last media query should kick in at a larger width
* Transitions are pretty jumpy

__HTML__
* Using forms for your submits
* BEM for the most part
* Don't forget to take out your commented out code
* Upon further reading, I think using a `<div>` may be the more semantically appropriate alternative to an `<hr>`. Good intuition!
* Good job using `for` attributes
  * Be consistent about it tho (line 53)
* Also be consistent about keep attributes on one line (lines 63/64)

__CSS__
* Good organization
* On occasion you have an unnecessary property in your styles (`align-items` on line 17)
* Be careful about consistently styling / spacing your file
* Rules on lines 407 / 411 can be combined (be careful about repetition)
* Could probably consolidate some of your input styling as well (colors, widths)

__JS__
* No event delegation
* Good organization of the JS
* Lots of handler functions
  * All named functions in the event listeners
* No nested conditional logic
* `winName` is undefined at pageLoad
  * would have wanted to use `#player-one` to querySelect it in the JS file
* Need some error validation to make sure that the border is disappearing
* You have some opportunity for refactoring your displaying functions on lines 179 and 184


### Functional Expectations

* Novice: Application meets all of the expectations of phase one.
* __Advanced Beginner:__ Application meets all of the expectations of phase two.
* Proficient: Application meets all of the expectations of phase three.
* Exceptional: Application adds three or more of the extensions from phase four.

------------------------------------------------------------------

### Comp Recreation

* Novice: Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)
* __Advanced Beginner:__ Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.). Transitions between screen sizes may not be smooth.
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
* Exceptional: Functions and code are well-refactored and show developer empathy and:
  * No global variables aside from query selectors, min & max, number of guesses, and start time
  * All functions are less than 10 lines
  * Uses logical operators instead of if/else statements where applicable
