## Student: Katie Williams and Hindreen Abdullah
## Evaluator: Khalid Williams
## Notes/What To Work On:

__General / Comp__
* Github workflow seems good

* Comp recreation looks really good
* Nice animations added to the cards being deleted / added
* Some overflow with the cards in mobile view
  * This is keeping you from proficient on comp recreation 

* Cards are adding
* Cards are delelting 
* Added delete all button 
* Timer is working on newly added cards
* Cards adding to the bottom of the column
* No range update on win
  * This is keeping you from proficient in the functional expectations  

* Follow the spec for what you need to make, don't get too ahead of yourself 

__HTML__
* Make sure to utilize the for attributes in your labels 
* Naming conventions are pretty clear
* No commented code, love to see it 
* The HTML looks pretty disorganized in terms of the indentation. This is worth going back and refactoring
* Do more research into the different semantic tags available to you (lots of `sections` and `divs`, look into `articles`, `forms`, etc ) 

__CSS__
* Organzized by page flow 
* Comments for organization
* Only one media 

__JS__
* Good organization
* Some code could be DRYed up a little bit
  * EX: `winnerOne()` and `winnerTwo()` functions
* Focus more on SRP princples in the future, some functions are pulling a lot more weight than they need to be
* Actually remove your cards from the DOM, don't just set their display to none
  * You're not fully taking advantage of event delegation, you don't just want to attach event listeners to each dynamically created element. Utilize event bubbling in the future
* Research other semantic tags that you could use for your cards, not just `div`s

### Functional Expectations

* Novice: Application meets all of the expectations of phase one.
* __Advanced Beginner:__ Application meets all of the expectations of phase two.
* Proficient: Application meets all of the expectations of phase three.
* Excpetional: Application adds three or more of the extensions from phase four.

------------------------------------------------------------------

### Comp Recreation

* Novice: Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)
* __Advanced Beginner:__ Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.). Transitions between screen sizes may not be smooth.
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