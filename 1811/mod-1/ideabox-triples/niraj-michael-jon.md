## Student: Niraj Aryal & Michael King-Stockton & Jon Keever
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Great work on the number of commits
  * In general, good improvement on making smaller commits.  Still several commits that combine HTML, CSS, and JS
  * Great start to branch names.  Continue to work on making them clearer and creating more branches
* A few things in the UI that could be spaced out better in the header such as the save button and quality buttons
  * Search and title could be centered vertically a bit better
  * Missing the line on the cards between the title/body and the quality/delete buttons
  * Not mobile friendly yet. Desktop things could fill out screen a bit better
* A few extra divs that could potentially be cleaned out in the header and form
* Could remove one of the spans in the title and style the h1 as a whole and then target one span
* Work on code readability including spacing between lines and tabbing in correctly
* Also be consistent with your class names using kabob case
* Cheers on organization of styles from top to bottom
  * Remember to alphabetize properties for each class
  * Might start using some percentages instead of so many pixels to make the site more responsive
* updateContent could be refactored using bracket notation
* Careful of nested if/else statements in updateQuality
  * Potentially instead of keeping track of each quality, try storing your qualities in an array and then only keeping track of the index in the constructor function
* Clean up console.logs in your javascript
  * Clean up comments as well in your code
* Continue to work on tabbing things in correctly in Javascript as well
  * Could use filter instead of for loop in search functionality
* For editing cards, instead of adding an event listener manually, use event delegation and attach an event listener on the entire section with all of the idea cards listening for focusout
* Refactor the upVote and DownVote function into one function
* PRACTICE TALKING THROUGH YOUR CODE!  Own it and know where things are.  Work on defending your decisions and how things are working.
* Again, check the styleguides as well and you're using kabob case for classes and make sure spacing & tabbing is correct!


### Functional Expectations

* [ ]  Proficient - Applications adds 'Filtering by Importance' and 'Recent Ideas' as outlined in the spec

------------------------------------------------------------------

### Comp Recreation

* [ ]  Novice - Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)

------------------------------------------------------------------

### HTML - Style and Implementation

* [ ]  Novice - Crafts markup according to the [turing html style guide](https://github.com/turingschool-examples/html)

------------------------------------------------------------------

### CSS - Style and Implementation

* [ ]  Advanced Beginner - Application adds organization for the whole stylesheet and within rules

------------------------------------------------------------------

### JAVASCRIPT - Style and Implementation

* [ ]  Advanced Beginner - Application adds to the above by correctly implementing a data model for the `Idea` class including all required methods

