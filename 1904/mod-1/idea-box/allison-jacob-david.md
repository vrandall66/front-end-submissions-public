## Student: Allison Wagner & Jacob Ogren & David Gitlen
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Great number of commits and being consistent with commit messages
  * Good number of branches, try to be a bit more specific with name of branches
* Great work on the filtering functionality
  * Slight bug with searching through ideas with qualities
* Very good attention to detail with the UI and UX
  * Would make sure inputs and buttons are same width as cards in all mobile layouts
* Remember your meta tag for mobile devices.
* Double check where tags are closing and tabbing
* In general good work on semantic tags 
* Good work breaking out the difference sections for each card
* Good organization of styles and alphabetizing properties
* See how you can use the shorthand for things like borders, margins, etc.
* Find places where classes are sharing similar styles and group them together
* Do we need to store the array of qualities in every instance?
* Careful of using multiple event listeners listening for same event
  * Example the window on line 21 & 22 & outputField on lines 29 & 32
* Can we do hovers more effectively using CSS?
* Good organization of global variables, event listeners, and function declarations
* How could we refactor handleCardEdit and focusOutEvent functions into one?
* Good scenario of using ternary for the star and which img to use
* Cheers to using the classList toggle method!

### Functional Expectations

*  Proficient: Application meets all of the expectations of phase three.

### Comp Recreation

*  Proficient - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward

### HTML - Style and Implementation

*  Proficient - Applications adds to the above with markup that is easy to read and follow across naming conventions

### CSS - Style and Implementation

*  Advanced Beginner - Application adds organization for the whole stylesheet and within rules

### JAVASCRIPT - Style and Implementation

*  Proficient - Application adds readability by incorporating both DRY and SRP practices and students can speak to implementation decisions and:
  *  Uses event delegation correctly on dynamic elements for deleting, editing, & starring an idea
  *  All functions are less than 10 lines
  *  There are no global variables aside from query selectors and two arrays for your ideas and qualities
  *  There are no nested if else statements