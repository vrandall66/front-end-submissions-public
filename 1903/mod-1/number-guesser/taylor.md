## Student: Taylor Jordan 
## Evaluator: Khalid Williams
## Notes/What To Work On:

__General / Comp__
* Commit more frequently, it gives you a safegaurd when it comes to dialing work 

* Comp recreation isn't quite there, general layout is good though
* Responsive to an extent

* Cards are adding to the page, errors are adding to the inputs but the SVG isn't there
* Can't delete the cards from the pages
* Two cards are always being added to the page when a user wins


__HTML__
* The indentation and structure of the html doc would be worth refactoring
* Naming conventions could be a little more specific
* Rmove commented out code 
* Research what semantic tags are available to you 

__CSS__
* Remove commented out code
* Organized based on page flow 
* Be consistent with the spacing between rules 
* **Refactor** this to remove commented out code and add in th econsistent spacing to work with the style guide

__JS__
* Used jquery for the form validation
* Submit and form validation function is pretty huge
  * There's opportunity to refactor this in to multiple smaller functions 
* In general, stay away from jquery. We want to make sure you're getting in the reps for what is happening under the hood with that library. jQuery is great, but it abstracts away too much of the code logic for you.
* You used anonymous functions with your event listeners, which is part of what's keeping you from an Advanced Beginner score
* Don't forget to remove your commented out code 

### Functional Expectations

* Novice: Application meets all of the expectations of phase one.
* __Advanced Beginner:__ Application meets all of the expectations of phase two.
  * You're close to a novice here becuase of the two-card addition bug 
* Proficient: Application meets all of the expectations of phase three.
* Exceptional: Application adds three or more of the extensions from phase four.

------------------------------------------------------------------

### Comp Recreation

* __Novice:__ Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)
  * The general layout is right, but the detail of the page is off from the comp

* Advanced Beginner: Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.). Transitions between screen sizes may not be smooth.
* Proficient: Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward.
* Exceptional: Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements that have been added match the visuals established in the comps.

------------------------------------------------------------------

### HTML - Style and Implementation

* Novice: Crafts markup according to the [turing html style guide](https://github.com/turingschool-examples/html)
* __Advanced Beginner:__ Application adds to the above with HTML that incorporates semantic HTML elements and has a simple, clean HTML structure.
  * Make sure you refactor the indentation 
* Proficient: Application adds to the above with markup that is easy to read and follows across naming conventions
* __Exceptional: Application adds to the above by using [BEM](http://getbem.com/), [SMACCS](https://smacss.com/), or another set of naming conventions for classes and:
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

* __Novice:__ Crafts JS according to the [turing js style guide](https://github.com/turingschool-examples/javascript/tree/master/es5)
* Advanced Beginner: Displays good understanding of arguments vs parameters and:
  * Uses function declarations over anonymous functions in event listeners
  * Uses if/else statements to handle multiple paths of logic/error handling
* Proficient: Application uses event delegation correctly on dynamic elements and:
  * Keeps functions DRY with a focus on SRP and can call functions within functions
  * There are no nested if/else statements
*  Exceptional: Functions and code are well-refactored and show developer empathy and:
  * No global variables aside from query selectors, min & max, number of guesses, and start time
  * All functions are less than 10 lines
  * Uses logical operators instead of if/else statements where applicable