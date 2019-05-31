## Student: Yana Aleksandrova, Sam Freeman, Julian Encohc-Brown
## Evaluator: Khalid Williams 
## Notes/What To Work On:

__General__
* Make sure everyone is getting an even number of commits on future projects 
* On the whole, good looking project. Small attention to detail aside, the desktop layout looked great. Code base was well organized and very tight. Everyone was able to discuss the code well 

__Comp Recreation__
* Desktop looks really good, barring a small issue with the card heights on big screens
* No responsiveness
  * This is what's keeping you at a novice for comp recreation 

__Functional Expectations__
* Adding, editing and removing cards 
* Starring also works 
* Searching by text also works
* Everything persists
  * Small bug in the favorite persistence, but on the whole stuff seems good 
* Through phase one, halfway through phase two
  * No quality changin

__HTML__
* Used template tages 
* Data attributes 
* Good naming conventions
* Add `for` attribute with your labels in the future 

__CSS__ 
* Good organization of the stylesheet 
* Good organization of the rules 
* no media queries, but the sheet looks well done 
* Nice job stack ing selectors and avioding redundancy 

__JS__
* Right number of global variables 
* JS file is really well organized 
* Good use of event delegation for deleting and favoriting 
* A small bug with favoriting beacuase of the star getting toggled every time the `updateIdea()` method, even when editing text


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