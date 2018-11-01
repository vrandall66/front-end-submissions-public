## Student: Kristen Hallstrom & Tiffany Bachmann
## Evaluator:
## Notes/What To Work On:
* Good start on more commits.  Make even more smaller commits!
  * Some funny commit messages, but make sure it's super clear on what functionality is being added/fixed.
  * Good start on branches as well, continue to make more branches as you make each commit
* Really love the drop down for the filter by ideas
* Really nice work storing one key with an array into localStorage
* Awesome UI and really great UX.  Very clean and easy to jump into
  * Quality buttons and text aren't quite vertically aligned
* Really nice work making sure things don't break depending on what the user does.  Cheers!
* Nice clean HTML structure
  * Good start on adding some accessibility
  * Some instances where we could use more semantic HTML
    * Like using h1 over p tag, form over section, or label of p tag next to input
    * Good start with adding accessibility to certain parts though including aria-labels
* Nice organization according to page flow with CSS and alphabetizing properties
  * Good use of grouping styles together that share similar properties.  A few other instances that could be grouped, but in general really good work!
* Nice work on your Idea class and using filter when trying to delete elements from localStorage array
  * Might not store the qualityIndex and quality since it gets a bit repetitive.  Store only the qualityIndex
  * Really good work with refactoring your upVote and downVote functionality.  
  * I might not hardcode the beginning and ending of array.  Imagine if you need to add more qualities.
* Really nice organization of main.js separating global variables, event listeners, and function declarations
* Good use of of array prototype methods over for loops
* Great work refactoring functions and breaking things out into smaller pieces
  * Super clean work with qualityFilter functionality and using the value from event.target
  * Think about how you could refactor the hiding and displaying functionality since that is done both in the Search and the qualityFilter function


### Functional Expectations

*  Proficient - Applications adds 'Filtering by Importance' and 'Recent Ideas' as outlined in the spec

### Comp Recreation

*  Exceptional - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements that have been added match the visuals established in the comps

### HTML - Style and Implementation

*  Proficient - Applications adds to the above with markup that is easy to read and follow across naming conventions

### CSS - Style and Implementation

*  Proficient - Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle

### JAVASCRIPT - Style and Implementation

*  Proficient - Application adds readability by incorporating both DRY and SRP practices and students can speak to implementation decisions and:
  *  All functions are less than 10 lines
  *  There are less than 3 global variables
  *  There are no nested if else statements