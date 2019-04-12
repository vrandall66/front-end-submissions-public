## Student: David Engel, Nathan Froehlich
## Evaluator: Khalid Williams
## Notes/What To Work On:

_General_
* Text is editable, adding and deleting persists, as well as favorites 
* Save button is disabled until both inputs filled in 
* Cards are appending to the center and then distributing to the fill out 
* No hamburger menu in the comp recreation
* Inputs don't clear out when we add a card to the DOM
* Utilizing grid might make the card flow more predictable 
* You have some awkward spacing below the "filter by quality" buttons; for sections like this, it;'s nicer looking if there's an even amount of white space above and below the text 

* Github looks pretty good 
* Pretty close number of commits, alhtough David had more lines added removed 


_HTML_
* Be consistent with the eway you're wriritng your attribute values (single vs double quotes")
* Good naming conventions  (based on BEM but not exactly that)
* Good use of semantic tags
* If you'd had data attributes in the idea cards, the HTML would be at a proficient

_CSS_
* Generally organized off of page flow
* Rules aren't very repetetive 

_JS_
* Still some issues with separation of DOM logic into the main.js file
  * shouldn't be calling `togglePrompt` in the idea.js file
* The rest of your JS is clean enough to be a proficient. However, you need to make sure you correctly keep your data methods free of DOM manipulation in the final projet. 
  * Likewise, don't have a `retrieveIdea()` function defined in your `idea.js` file -- that should __only__ have the Idea class in it
  * Really focus on separating the the DOM and data logic for Check Yo'Self


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
*  __Advanced Beginner - Application adds to the above by using appropriate semantic elements and using `data-*` attributes for all data related things__
*  Proficient - Applications adds to the above with markup that is easy to read and follow across naming conventions
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