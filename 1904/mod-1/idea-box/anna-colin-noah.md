## Student: Annie Goodwin, Colin Koga, Noah Gibson 
## Evaluator: Khalid Williams 
## Notes/What To Work On:

__General__ 
* github commits were looking pretty good 
  * Well structureed 

__Comp Recreation__
* not fully responsive
* UI is a little rough around the edges 

__Functional__
* Can add, edit and deleting ideas 
  * Edits of ideas do not persist across page refresh 
* Save button is disabled when it needs to be 

__HTML__
* Scripts importing in the right order 
* Used a nav for the side bar 
* `for` attributes with lavbels aren;t set up quite right -- needs to correspond to `id`, not `name`
* Using data attributes 

__CSS__ 
* Following page flow 
* Alphabetization of the rules 
* Some redundant rules with the inactive buttons
  * Don't forget you can stack selectors

__JS__ 
* PRetty good organization of the file 
* Right amount of global variables 
* Could DRY up your event listeners -- in fact, you did, but you need to 

### Functional Expectations

*  __Novice: Application meets all of the expectations of phase one.__
*  Advanced Beginner: Application meets all of the expectations of phase two.
*  Proficient: Application meets all of the expectations of phase three.
*  Exceptional: Application adds all of the extensions from phase four.

### Comp Recreation

*  __Novice - Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)__
*  Advanced Beginner - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.). Transitions between screen sizes may not be smooth
*  Proficient - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward
*  Exceptional - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements that have been added match the visuals established in the comps

### HTML - Style and Implementation

*  Novice - Crafts markup according to the turing html style guide
*  Advanced Beginner - Application adds to the above by using appropriate semantic elements and using `data-*` attributes for all data related things
*  __Proficient - Applications adds to the above with markup that is easy to read and follow across naming conventions__
*  Exceptional - Application adds to the above by using BEM, SMACCS, or another set of naming conventions for classes and:
  *  Implements html that is accessible for folks with visual disabilities.

### CSS - Style and Implementation

*  Novice - Crafts CSS according to the turing css style guide
*  __Advanced Beginner - Application adds organization for the whole stylesheet and within rules__
*  Proficient - Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle
*  Exceptional - Application adds to the above by using BEM, SMACCS, or another set of naming conventions for classes

### JAVASCRIPT - Style and Implementation

*  Novice - Crafts JS according to the turing js style guide
*  Advanced Beginner - Application adds to the above by correctly implementing a data model for the `Idea` class including all required methods
*  Proficient - Application adds readability by incorporating both DRY and SRP practices and students can speak to implementation decisions and:
  *  Uses event delegation correctly on dynamic elements for deleting, editing, & starring an idea
  *  All functions are less than 10 lines
  *  There are no global variables aside from query selectors and two arrays for your ideas and qualities
  *  There are no nested if else statements
*  Exceptional - Application adds to code quality by refactoring all for loops into the proper array prototype iteration methods and:
  *  Uses logical operators instead of if/else statements where applicable
  *  Uses arrow functions, block scoped variables, and destructuring correctly.
  *  When 'Filtering and Searching by Text' and 'Filtering by Importance', ideas that do not need to be shown on the dom should be completely removed from the dom, instead of only being hidden from view