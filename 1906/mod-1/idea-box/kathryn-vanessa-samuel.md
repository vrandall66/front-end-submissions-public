## Student:
## Evaluator:
## Notes/What To Work On:

__General__
* Search functionality was a bit of a struggle, but they got there!
* Can add and save ideas
* Can search by text
* Persisting on page refresh
* Can delete cards
* Cards are editable


__Comp__
* Have hover states
* Custom cursors
* Hamburger menu is there but not function


__Functional Expectations__


__HTML__
* Indentation is a little funky in a few spots
* Using a BEM-like structure for naming conventions
* Make sure the code styling is consistent and in line with the style guide
* Using data attributes


__CSS__
* Rules are organized by DOM section and page flow
* PRoperties are alphabetized
* Some areas where you could dry things up in the CSS
  * We talked about the repeated properties in the

__JS__
* Good organization of the page
* Using the global array in the idea.js methods
* Increase and decrease quality functions could be refactored to be one function
  * Aside from this, you're right about at proficient

### Functional Expectations

*  Novice: Application meets all of the expectations of phase one.
*  __Advanced Beginner:__ Application meets all of the expectations of phase two.
*  Proficient: Application meets all of the expectations of phase three.
*  Exceptional: Application adds all of the extensions from phase four.

### Comp Recreation

*  Novice - Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)
*  Advanced Beginner - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.). Transitions between screen sizes may not be smooth
*  __Proficient__ - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward
*  Exceptional - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements that have been added match the visuals established in the comps

### HTML - Style and Implementation

*  Novice - Crafts markup according to the turing html style guide
*  Advanced Beginner - Application adds to the above by using appropriate semantic elements and using `data-*` attributes for all data related things
*  __Proficient__ - Applications adds to the above with markup that is easy to read and follow across naming conventions
*  Exceptional - Application adds to the above by using BEM, SMACCS, or another set of naming conventions for classes and:
  *  Implements html that is accessible for folks with visual disabilities.

### CSS - Style and Implementation

*  Novice - Crafts CSS according to the turing css style guide
*  __Advanced Beginner__ - Application adds organization for the whole stylesheet and within rules
*  Proficient - Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle
*  Exceptional - Application adds to the above by using BEM, SMACCS, or another set of naming conventions for classes

### JAVASCRIPT - Style and Implementation

*  Novice - Crafts JS according to the turing js style guide
*  __Advanced Beginner__ - Application adds to the above by correctly implementing a data model for the `Idea` class including all required methods
*  Proficient - Application adds readability by incorporating both DRY and SRP practices and students can speak to implementation decisions and:
  *  __Uses event delegation correctly on dynamic elements for deleting, editing, & starring an idea__
  *  __All functions are less than 10 lines__
  *  __There are no global variables aside from query selectors and two arrays for your ideas and qualities__
  *  __There are no nested if else statements__
*  Exceptional - Application adds to code quality by refactoring all for loops into the proper array prototype iteration methods and:
  *  Uses logical operators instead of if/else statements where applicable
  *  Uses arrow functions, block scoped variables, and destructuring correctly.
  *  When 'Filtering and Searching by Text' and 'Filtering by Importance', ideas that do not need to be shown on the dom should be completely removed from the dom, instead of only being hidden from view
