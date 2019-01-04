## Student: Jake Admire & Taylor Sperry & Josh Lavarine
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Excellent work on the number of commits
  * Great work on small atomic commits.  Please keep this up!
  * Great work on your branch names as well.  Cheers!
* Great work on your UX/UI
  * Really love the hamburger icon that opens up the buttons
  * A few things on spacing that could be improved on to match the comp exactly but in general very very solid
  * A few times the text like Plausible gets knocked down depending upon the window size
* Might use a form and label around the search input
* Instead of using divs for the hamburger icon, use an svg icon
* Careful of the amount of divs being used when appending each idea 
  * Could use section/article
  * Instead of overlay, try targeting with CSS and if you want to change color of image, replace the image
* Good organization of styles and alphabetizing properties
* Good work grouping classes with similar styles together (If more than 3 classes are being grouped together, use one class)
* Still some areas that could be dried up that share similar traits
* Careful of using position relative on the header in the media query
* updateContent should update the properties in the constructor function
* Good organization of global variables, event listeners, and function declarations 
* Careful of multiple event listeners on the section
  * Good start to trying to combine them into one
* Cheers to using forEach on the reloadCards function
* A bit confusing to using createElement but then also adding innerHTML to it.  Use one or the other.  I recommend using document.createElement() only if it's one element you are trying to append such as a button
* Since you are treating your ideas as an array, try storing it into localStorage as an array
* Instead of clearing out the entire DOM when searching try removing only the cards you need to remove
* For increasing/decreasing quality, instead of checking to see if the innerText is a particular value, store your qualities in an array and keep track of the index in the array.  Then you can increment/decrement based on clicking up or down
  * This will also help remove the nested if/else statements
* Instead of doing .parentElement multiple times, look into the method closest()
* A few things that could be cleaned up in the editing
  * Could remove the !error return conditional
  * Could go after event.target.value instead of grabbing foundIdea.title or body

### Functional Expectations

* [ ]  Advanced Beginner - Application adds 'Changing the quality of an idea' and enables 'Filtering and Searching by Text' as defined in the spec

------------------------------------------------------------------

### Comp Recreation

* [ ]  Proficient - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward

------------------------------------------------------------------

### HTML - Style and Implementation

* [ ]  Proficient - Applications adds to the above with markup that is easy to read and follow across naming conventions

------------------------------------------------------------------

### CSS - Style and Implementation

* [ ]  Proficient - Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle

------------------------------------------------------------------

### JAVASCRIPT - Style and Implementation

* [ ]  Advanced Beginner - Application adds to the above by correctly implementing a data model for the `Idea` class including all required methods

