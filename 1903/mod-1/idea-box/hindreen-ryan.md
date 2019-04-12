## Student: Hindreen Abdullah, Ryan Flachman
## Evaluator: Khalid Williams
## Notes/What To Work On:

_General_
* Github looks good 
* Make sure to always capitalize your commit messages 
* Pretty even contributions on the insights pages
* Eventually started splitting out tasks after getting a common foundation 

* Cards are persisiting 
* Got character counters working 
* Can change quality 
* Can edit cards 
* Can favorite 
* Can show starred ideas, but the button text doesn't toggle
* Can filter by importance 
* Some confusion on what the filter by text spec was asking for 

* Responsive down to 320 
* Some askward sizing on the small screen wirth the card width 
* Hamburger menu is working 
* You have a strange pink border around your `sidebar` and `main__bottom-section`
  * I trust these were for setting the original grid areas, but don't leave them in 

_HTML_
* Using BEM 
* Split page into a section and a main
* Could look into more semantic tags to use (aside, nav), worth researching more 
* Using data attributes 
* If you'd made everyting tabbable or added `aria` atrtibutes for accessbility, this would have been around an exceptional

_CSS_
* BEM allowed for a very clean structure
* Only one media query
 

_JS_
* Only two global varaibels aside from  querySelectors 
* No delete from storage method in the Idea class 
* Using event delegation 
* Doing some redundant work when removing your card because of calling the local storage method in your map function
  * This is a good example of why to keep the storage and data manipulation in the Idea class -- you won't run into reduncancies like that by mistake as much


### Functional Expectations

*  Novice: Application meets all of the expectations of phase one.
*  __Advanced Beginner: Application meets all of the expectations of phase two.__
*  Proficient: Application meets all of the expectations of phase three.
*  Exceptional: Application adds all of the extensions from phase four.

### Comp Recreation

*  Novice - Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)
*  Advanced Beginner - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.). Transitions between screen sizes may not be smooth
*  __Proficient - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward__
*  Exceptional - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements that have been added match the visuals established in the comps

### HTML - Style and Implementation

*  Novice - Crafts markup according to the turing html style guide
*  Advanced Beginner - Application adds to the above by using appropriate semantic elements and using `data-*` attributes for all data related things
*  __Proficient - Applications adds to the above with markup that is easy to read and follow across naming conventions__
*  Exceptional - Application adds to the above by using BEM, SMACCS, or another set of naming conventions for classes and:
  *  Implements html that is accessible for folks with visual disabilities.

### CSS - Style and Implementation

*  Novice - Crafts CSS according to the turing css style guide
*  Advanced Beginner - Application adds organization for the whole stylesheet and within rules
*  Proficient - Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle
*  __Exceptional - Application adds to the above by using BEM, SMACCS, or another set of naming conventions for classes__

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