## Student: Brianna DelValle and Brandy Mello 
## Evaluator: Khalid 
## Notes/What To Work On:

__General__
* Don't leave refactoring to the last minute
* Git and github collaboration looks good 
* Lots of coauthored commits 
* Readme looks great

__Comp Recreation__
* Looks good on mobile and desktop
* Smooth transitions between breakpoints
* A few areas where you could have used more attention to detail 
  * Not having the error messages bump content around the page 
  * Delete buttons on the cards are not totally in line with the guesses and timestamps 
    * A bit of extra space on the bottom of the cards as well 

__Functional__ 
* Error message are adding and looking good / consistent 
  * Errors are not dissappearing on reset 
    * Might need a listener on the `change` or `input` event 
* Cards are deleting 
* Error message consistency aside (not dissappearing on reset), everything is through phase three  


__HTML__
* Semantic tags
* using forms for the input sections 
* Article for the scoreboard 
* Using alt tags 
* Using for labels 
* Be careful about leaving in name attributes 

__CSS__
* More or less organized by functionality and specificity
* Naming conventions make the lose organization usable, but hte stylesheet could use more organization 
  * Merge conflict was the culprit of the lack of organzation, not enough time to refactor it 

__JS__
* Good organization of page 
* No anonymous fncs in the event listeners 
* Room for refactoring with the runName and runGuess functions
  * Students were aware of opportunities when prompted about them
  * Think about how we can utilize parameters to avoid having repettive functions
* Think about places helper functions can shorten up your functions by removing repetive operations
* The room for making your functions more dry is what's keeping you from a profcient in the JS. On the whole, this project look graet, though. 


### Functional Expectations

* Novice: Application meets all of the expectations of phase one.
* Advanced Beginner: Application meets all of the expectations of phase two.
* __Proficient:__ Application meets all of the expectations of phase three.
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