## Student: Colin Koga and Garret Iannuzzi
## Evaluator: Khalid Williams
## Notes/What To Work On:

__General__
* Felt like a lot of their mental energy went to resoliving conlficts due to Git 
* Fix broken links on your readme
* Put a link to your live site on the readme 

__Comp Recreation__
* Error messages are very tiny
* A few attention to detail issues 
  * Range is not underlined or bolded as it is in the comp 
* Card UI is pretty basic 
* Styling doesn't reflect the disabled button states 
* Somewhat responsive, no buttons stacking 
  * Make sure you pay attention to all details of the comp when styling things 

__Functional__ 
* Error messages populating for the range inputs 
* Buttons are disabled when inouts are initially empty, but not disabling dynamically (ex after clearing an input)
  * Attaching the function to amn 

__HTML__
* Naming needs to be more consistent
* Don't use camelCase in your html 
* Remove your commented out code
* A form would be a more semantic option for your input areas 

__CSS__
* Generally ortganized by source code order 
* For the most part, no repetive rules
* One media query, needs more styling in it  

__JS__
* Style and structure of the page needs some attention 
  * spacing / indentation is not consisent, make sure you're paying attention to the Turing style guide 
* Plenty of room to refactor things 
* You could use a for loop to shorten your clearn inputs functions 
* Think about the loginc in your disable inputs function. What happens if only one input has text in it?
* Keep your event listeners and query selectored organized to the same places 
* 


### Functional Expectations

* __Novice:__ Application meets all of the expectations of phase one.
* Advanced Beginner: Application meets all of the expectations of phase two.
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