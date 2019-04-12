## Student: Emily LaLonde, Andreea Hanson, Anneke McGrady
## Evaluator: Khalid Williams
## Notes/What To Work On:

_General_
* github looks good 

* Cards are saving and persisting 
* Search by text is working 
* Editing cards working
* Cannot change quality but can favorite
  * Favorites aren't perisisting 
* Make sure you're using the rubric to guide which functionality you're working on 
  * Don't be afraid to pair on the trickier things that come earlier in the rubric
* Need to reload page or hover over a card for "please enter an idea" message to appear or dissapear



_HTML_
* Good use of semantic tags 
  * Not sure if the aside is entrely necessary
  * It seems you could just use the `nav` and asign it to the grid area of `aside` you used, as well as giving it the dark purple background color 
* Nice clean naming conventions
* Using data-attributes!


_CSS_
* A good number of media queries 
  * might not need all the large screen ones, feels a bit liek micro managing 
* Repetitve rules in the media queries -- you got smooth transitions, but be careful that you aren't repeating yourself by doing so

_JS_
* A little bit of commented out code
* Don't forget to take out your console.logs
* Good job using event delegation for your deleting 
* You need to dynamically change the star icon when you `restoreIdeas` from localStorage to the DOM
  * The star property is persisting, but every time you run `populateCard` you load an unfavorited star icon. 


### Functional Expectations

*  __Novice: Application meets all of the expectations of phase one.__
*  Advanced Beginner: Application meets all of the expectations of phase two.
*  Proficient: Application meets all of the expectations of phase three.
*  Exceptional: Application adds all of the extensions from phase four.

### Comp Recreation

*  Novice - Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)
*  __Advanced Beginner - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.). Transitions between screen sizes may not be smooth__
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
*  __Proficient - Application adds readability by incorporating both DRY and SRP practices and students can speak to implementation decisions and:__
  *  Uses event delegation correctly on dynamic elements for deleting, editing, & starring an idea
  *  All functions are less than 10 lines
  *  There are no global variables aside from query selectors and two arrays for your ideas and qualities
  *  There are no nested if else statements
*  Exceptional - Application adds to code quality by refactoring all for loops into the proper array prototype iteration methods and:
  *  Uses logical operators instead of if/else statements where applicable
  *  Uses arrow functions, block scoped variables, and destructuring correctly.
  *  When 'Filtering and Searching by Text' and 'Filtering by Importance', ideas that do not need to be shown on the dom should be completely removed from the dom, instead of only being hidden from view