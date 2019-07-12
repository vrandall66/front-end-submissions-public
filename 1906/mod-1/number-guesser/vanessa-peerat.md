## Student: Vanessa Randall and Peerat Sukcharoenyingyong
## Evaluator: Khalid Williams
## Notes/What To Work On:

__General__
* Error messages coming through
  * No borders getting added to the input on error
* Cards getting added to the page
* Range is updating on win
* Can still submit without a name

__Comp__
* First breakpoint could have left some inputs a little bit bigger, leaving a lot of space in the challenger section
* Need pink border on error message

__HTML__
* BEM-like naming conventions
* Using for attributes
  * Don't forget to match these to the `id` of the corresponding element (on lines 28 & 29 you're matching it to a `name` attribute)
* Could opt for `forms` over `sections` in your user input areas


__CSS__
* Don't forget to take out your comments!!
* Rule organization is a little hairy
  * Alphabetized for the most part
  * Has flex properties at the top of the rules
* Think about making a flex class to shorten up the CSS a bit
* Good job stacking selectors
* A little bit of repetition in the media queries

__JS__
* Good organization of the file
* No event delegation being taken advantage of
* No huge functions
* Could refactor your checkInput functions to only be one
  * Same thing with guessWithinRange functions
* Inner HTML being added can be structured as though it were an actual element
  * Use multiple lines for readability!


### Functional Expectations

* Novice: Application meets all of the expectations of phase one.
* __Advanced Beginner:__ Application meets all of the expectations of phase two.
* Proficient: Application meets all of the expectations of phase three.
* Exceptional: Application adds three or more of the extensions from phase four.

------------------------------------------------------------------

### Comp Recreation

Novice: Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)
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
