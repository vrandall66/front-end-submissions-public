## Student: Garrett Iannuzzi, Djavan Munroe, Edward Cheatam
## Evaluator: Khalid Williams 
## Notes/What To Work On:

__General__
* Used a lot of agile practices in setting up the division of labor 
* Everyone feels communiation was good 
* A bit of an uneven amount of commits

__Comp Recreation__
* things look good 
* Responsive down to a mobile layour 
* A few issues with attention to detail (not spacing between quality filter and border in the hover state)
* Hamburger menu is not functional, but the layout reflects the comp
* Tranisitions are a little awkward with font sizes jumping around

__Functional Expectations__
* Things are up through phase three 

__HTML__
* Using data attributes 
* BEM for naming conventions 
* Could speak to choices regarding accessibility 
__CSS__ 
* Good organization of the CSS
* Using BEM
* General organization by page flow 
* Properties are alphabetized 
* Lots of relative units 
* Seems like BEM allowed them to not have to stack selectors

__JS__
* Nice general organization of the JS 
* Functions generally organized by feature, but could use a bit more rganization 
* Could clean things up by grouping your bottom container event listeners into their own functions
  * The reason this may not hav eworked before could have been forgetting to pass the event object down into your functions?
* Cool solution for filtering via the DOM
* The code base is pretty heavy with array prototypes -- nice way to get your feet wet 
* Most functions are less than 10 lines -- you stacked things for readability, so I'll let it pass this time 
  * In general, you don't need to break things in the JS out in to too many lines if the statement is readable (ex: your `or operators` on lines 123 and 124)

### Functional Expectations

*  Novice: Application meets all of the expectations of phase one.
*  Advanced Beginner: Application meets all of the expectations of phase two.
*  __Proficient: Application meets all of the expectations of phase three.__
*  Exceptional: Application adds all of the extensions from phase four.

### Comp Recreation

*  Novice - Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)
* __Advanced Beginner - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.). Transitions between screen sizes may not be smooth__
*  Proficient - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward
*  Exceptional - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements that have been added match the visuals established in the comps

### HTML - Style and Implementation

*  Novice - Crafts markup according to the turing html style guide
*  Advanced Beginner - Application adds to the above by using appropriate semantic elements and using `data-*` attributes for all data related things
*  Proficient - Applications adds to the above with markup that is easy to read and follow across naming conventions
*  __Exceptional - Application adds to the above by using BEM, SMACCS, or another set of naming conventions for classes and:__
  *  Implements html that is accessible for folks with visual disabilities.

### CSS - Style and Implementation

*  Novice - Crafts CSS according to the turing css style guide
*  Advanced Beginner - Application adds organization for the whole stylesheet and within rules
*  __Proficient - Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle__
*  Exceptional - Application adds to the above by using BEM, SMACCS, or another set of naming conventions for classes

### JAVASCRIPT - Style and Implementation

*  Novice - Crafts JS according to the turing js style guide
*  Advanced Beginner - Application adds to the above by correctly implementing a data model for the `Idea` class including all required methods
*  __Proficient - Application adds readability by incorporating both DRY and SRP practices and students can speak to implementation decisions and:__
  *  Uses event delegation correctly on dynamic elements for deleting, editing, & starring an idea
  *  All functions are less than 10 lines
  *  There are no global variables aside from query selectors and two arrays for your ideas and qualities
  *  There are no nested if else statements
*  Exceptional - Application adds to code quality by refactoring all for loops into the proper array prototype iteration methods and:
  *  Uses logical operators instead of if/else statements where applicable
  *  Uses arrow functions, block scoped variables, and destructuring correctly.
  *  When 'Filtering and Searching by Text' and 'Filtering by Importance', ideas that do not need to be shown on the dom should be completely removed from the dom, instead of only being hidden from view