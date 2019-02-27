## Student: Melissa LaChasse & Colby Allen & Lynne Rang
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Good work on number of commits and branches
* In general, good consistency with branch names (careful of dashes and underscores)
  * Keep working on consistency with imperative tense for commits
* Good attention to detail with the UX and UI
  * Really good spacing between elements and being consistent
* Careful of flashiness when appending the cards
* In mobile view, I might make the buttons more like a drop down
* Good work adding accessbility to your HTML and attention to detail
* Careful of inline functions in your HTML
* Good organization with properties 
  * Remember to alphabetize your properties
* See how you can refactor your media queries so there isn't quite as much micro-management
* A few global variables that could be locally scoped like qualityTerms, cardsHidden, & currentCardList
* Could use bracket notation for the updateContent method in the Idea class
* Be consistent with the type of functions in your event listeners using function declarations over anonymous functions
* See how you can refactor the quality buttons so you don't have to pass a number through when it's invoked
* Good work refactoring the changeQuality function and keeping the track of the index
  - I would move the logic of updating the quality into the class.  So it might be something like `this.quality++`
* Functions like overTenCards do not need to be in it's own function.  This can be the expression in your conditional.
* Essentially did event delegation, but remember to put the event listener on the parent section (DON'T do inline functions)
* For onSearchToggle function, look into how you can refactor this using the `toggle` method for classList.

### Functional Expectations

*  Exceptional - Application adds all of the extensions

### Comp Recreation

*  Exceptional - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements that have been added match the visuals established in the comps

### HTML - Style and Implementation

*  Proficient - Applications adds to the above with markup that is easy to read and follow across naming conventions

### CSS - Style and Implementation

*  Proficient - Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle

### JAVASCRIPT - Style and Implementation

*  Advanced Beginner - Application adds to the above by correctly implementing a data model for the `Idea` class including all required methods
