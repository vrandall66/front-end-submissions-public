## Student: Eric Meldrum, Chris Basham
## Evaluator: Khalid Williams
## Notes/What To Work On:

__General__
* Add link to the live site on your README.md!
* Chris did most of the HTML and CSS
* Eric did most of the JS?
* Make sure you're both getting an even amount of time working each part of the
* Be specific with error messages (e in the input fields)
* No range update on win
* Cards getting added to the page
  * No number of guesses but the delete is working


__Comp__
* Error message styling isn't quite there
  * Had some issue with their last push?
* Cards get a little squirrelly on big screens
* Mobile view is there, the transition is a little jumpy
* The styling on your submit buttons gets a little wonky around 1130px


__HTML__
* Tab size is 4 -- should be 2
* Need to make `for` attributes in your label tags  
* Indentation is a little off
* Using inline event listeners
  * Stay away from this for now -- refactor over the weekend
  * We want to emphasize keeping structure, behavior, and styling all in their own respective files
* Nice use of `fieldset`
* Why are you using `name` attributes?
* Make sure to consistently use `kabob-case` in your


__CSS__
* Can refactor with some stacked selectors -- a bit of repetition right now (inputs around line 138)
* three media queries
* Properties stop being consistently alphabetized around line 167

__JS__
* Need to take out your console logs
* Could refactor things to be more dynamic
* TAKE OUT YOUR CONSOLE.LOGS

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
* __Advanced Beginner:__ Application adds to the above with HTML that incorporates semantic HTML elements and has a simple, clean HTML structure.
* Proficient: Application adds to the above with markup that is easy to read and follows across naming conventions
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
