## Student: Scott Schipke, Eduardo Rodrigo, Annie Olsen
## Evaluator: Khalid
## Notes/What To Work On:
__General__
* Sounds like you really built out a great process
* GitHub looks good
* Lots of retros and standups

__Comp__
* Desktop looks good, a few areas there some sizing is a little off from the comp (inputs cold be a little wider )
* Have hover states
* Good transitions between the media queries


__Functional Expectations__
* Adding and deleting works and persists
* Text and starred filtering work, along with quality filtering
* Can change quality
* Disabling save button when inputs are empty
* Good text prompts in your card area

__HTML__
* Using BEM-like structure
* Using alt tags and for attributes
* Using data attributes

__CSS__
* Generally organized by page flow
* properties are alphabetical
* Only 2 media queries
* In general, don't over-stack selectors 

__JS__
* Good organization of the file
* Everyone seems to be able to speak to the pieces of functionality
* Using a lot of handler functions for their dynamic content


### Functional Expectations

*  Novice: Application meets all of the expectations of phase one.
*  Advanced Beginner: Application meets all of the expectations of phase two.
*  __Proficient:__ Application meets all of the expectations of phase three.
*  Exceptional: Application adds all of the extensions from phase four.

### Comp Recreation

*  Novice - Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)
*  Advanced Beginner - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.). Transitions between screen sizes may not be smooth
*  __Proficient__ - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward
*  Exceptional - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements that have been added match the visuals established in the comps

### HTML - Style and Implementation

*  Novice - Crafts markup according to the turing html style guide
*  Advanced Beginner - Application adds to the above by using appropriate semantic elements and using `data-*` attributes for all data related things
*  Proficient - Applications adds to the above with markup that is easy to read and follow across naming conventions
*  __Exceptional__ - Application adds to the above by using BEM, SMACCS, or another set of naming conventions for classes and:
  *  Implements html that is accessible for folks with visual disabilities.

### CSS - Style and Implementation

*  Novice - Crafts CSS according to the turing css style guide
*  Advanced Beginner - Application adds organization for the whole stylesheet and within rules
*  __Proficient__ - Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle
*  __Exceptional__ - Application adds to the above by using BEM, SMACCS, or another set of naming conventions for classes

### JAVASCRIPT - Style and Implementation

*  Novice - Crafts JS according to the turing js style guide
*  Advanced Beginner - Application adds to the above by correctly implementing a data model for the `Idea` class including all required methods
*  __Proficient__ - Application adds readability by incorporating both DRY and SRP practices and students can speak to implementation decisions and:
  *  Uses event delegation correctly on dynamic elements for deleting, editing, & starring an idea
  *  All functions are less than 10 lines
  *  There are no global variables aside from query selectors and two arrays for your ideas and qualities
  *  There are no nested if else statements
*  Exceptional - Application adds to code quality by refactoring all for loops into the proper array prototype iteration methods and:
  *  __Uses logical operators instead of if/else statements where applicable__
  *  Uses arrow functions, block scoped variables, and destructuring correctly.
  *  __When 'Filtering and Searching by Text' and 'Filtering by Importance', ideas that do not need to be shown on the dom should be completely removed from the dom, instead of only being hidden from view__
