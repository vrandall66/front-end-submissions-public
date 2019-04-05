## Student: Jon O'Drobinak and Anneke McGrady
## Evaluator: Khalid 
## Notes/What To Work On:

__General / Comp__
* Felt like things were a little up and down
* Jon feels liek some things didn't get where he wanted to
* Things for next time: 
  * Better communication 
  * Better plan fro the get go 
  * Better organization for how to approach the work
* Put a link to your live site in the ReadMe

* Can update range
* Can only add one new winner
* Error messages are adding, but squishing the inputs up when they're added
*  Responsiveness works on Jon's but not on the github pages

__HTML__
* Figure out how to make your header layout not need FPO text
* Don't overuse sections
  * Research more semantic tags that are available to you 
* Utilize DOM manipulation instead of hiding the winning card -- this will allow you to add more than one card to the history section 
* Refactor the indentation -- it's hard to tell the structure of the code by looking at it
* Avoid inline styles 
* Be consistent with the spacing in your attributes: `<element attribute="value" />` would be the general way to style things



__CSS__
* Make sure to remove any commented out code 
* The error SVGs are causing the inputs to move around becuase you're using `display: none` rather than `visibility: hidden`
* Keep the spacing consistent in your CSS rules 
* Try and avoid using moer than 5 selectors for a rule -- usually that means you could add another class to the elements being selected



__JS__
* Organization is a little unclear with all the comments
* Make sure all the event listeners and query selectors are in the same place 
* Some functions could be dryed up a good amount (boomOne and boomTwo, guessErrorOne and guessErrorTwo)
* In the future, remove console.logs and commented out code 
* Comments used for organization should be minimalist 
  * Don't need a comment to explain ech query selector, the variable names  
* Try and focus on using named functions rather than anonymous ones 


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

* __Novice:__ Crafts markup according to the [turing html style guide](https://github.com/turingschool-examples/html)
* Advanced Beginner: Application adds to the above with HTML that incorporates semantic HTML elements and has a simple, clean HTML structure.
* Proficient: Application adds to the above with markup that is easy to read and follows across naming conventions
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