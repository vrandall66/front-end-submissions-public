## Student: Menashe Borukhov & Kelly Zick & Brennan Duffey
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Good work on number of branches and commits
* Good consistency of branch names and commit messages
* Good spacing of elements and sizing of fonts
* Might see how we can utilize more of the space on bigger screens for 
* Good work keeping HTML semantic and keeping the structure clean
* Good organization of styles and alphabetizing properties 
* A few too many places of using position relative and abosolute, see how you can get it behave without it
* Got similar functionality in deleteFromStorage, updateContent, and updateQuality in class (some pieces of functionality that could get moved over from the main.js into the idea.js)
  - For example, in the editCardText function we could move the logic of updating the title and body into the class `this.title = text`
* Good organization of global variables, event listeners, and function declarations
* Good work using event delegation
* Make sure function names are a verb describing the action
* Good start creating the quality array (could make this local instead of global)
  - Keep track of the index of the quality in the class so you don't have to manually check if the quality is a specific value
  - Could refactor the increaseQuality and decreaseQuality into one after this
- In the onPageLoad function, we actually do not need a conditional to see if the array.length is greater than 10.  Slice will not throw an error even if there are not 10 values in the array (it will just grab what is in there)
* Good work with the filterByQuality function and filtered by e.target.innerText
- Could combine the typeSearch function and searchIdeas function into one

### Functional Expectations

*  Proficient - Applications adds 'Filtering by Importance' and 'Recent Ideas' as outlined in the spec

### Comp Recreation

*  Proficient - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward

### HTML - Style and Implementation

*  Proficient - Applications adds to the above with markup that is easy to read and follow across naming conventions

### CSS - Style and Implementation

*  Proficient - Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle

### JAVASCRIPT - Style and Implementation

*  Advanced Beginner - Application adds to the above by correctly implementing a data model for the `Idea` class including all required methods