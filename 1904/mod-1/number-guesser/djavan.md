## Student: Djavan Munroe
## Evaluator: Khalid Williams 
## Notes/What To Work On:
__General__
* Time management was an issue
  * Need to make refactoring a consistent part of the workflow, as wel as testing
* Utilize the rubric to keep the time management together 
 
__Comp Recreation__
*  Some spacing issues with the latest score scetion, may be using margin instead of padding to get the spacing there 
* Media queries are a little busted 
  * not giving the left side a the full width of the page
* The spacing on the cards should be the equal with the input spacing when viewing things in mobile  

__Functional__ 
* Input validation errors are working 
* Range is updating on win 
* Cards adding and deleting
* Up through phase three

__HTML__
* Using an aside for the winning card area 
* Organzing input areas into forms 
* Naming conventions are clear, but could be more consistent in terms of how they are written (ex `player-one` vs `p1`)

__CSS__
* No reset and normalize 
* some redundant rules (over-slecting with such as with the `input.playerOne/playerTwo` area)
* Prioritize your styling dfrom the start next time 
* Be realistic with your screen sizes when writing media queries 

__JS__
* Good ogranziation of the JS
* A lot of repetitive functions that could be refactored 
* Good use of arguments and parameters in many places
* You used event delegation correctly, but the code isn't quite dry enough to be considered a proficient
  * Think about functions like `enableClear` and `disableClear`; this could easily be one toggleClear function that would still be considered singly responsible. There are multiple functions to which this logic could be applied
  * In the future, try and add in more periodic times for refactoring JS and HTML / CSS, so you don't end up pressed for refactoring time at the end 

### Functional Expectations

* Novice: Application meets all of the expectations of phase one.
* Advanced Beginner: Application meets all of the expectations of phase two.
* __Proficient:__ Application meets all of the expectations of phase three.
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
*  Exceptional: Functions and code are well-refactored and show developer empathy and:
  * No global variables aside from query selectors, min & max, number of guesses, and start time
  * All functions are less than 10 lines
  * Uses logical operators instead of if/else statements where applicable