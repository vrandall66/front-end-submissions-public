## Student: Kayla Larson & Edward Cheatham & Taylor Jordan
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Fantastic number of commits
* Good work with commit messages and using the imperative tense
* Could likely have a few more branches, make sure to be consistent with kabob case
* Card should appear in the upper left hand corner 
* Make sure the application takes up the entire height on all screens
* Couple of things slightly off on comp like the search button on the input.
  * New Quality label and input should be stacked on top of each other
  * Buttons and qualities could be a little taller
  * Color of hrs are a bit off
* Spacing on the side-bar shrinks more and more as the screen squishes
* Good work getting the menu to work 
  * Make sure the menu button is centered vertically
  * Menu icon should also change to an x when menu is open
* Make sure buttons and inputs align and are the same width
* Remember to link your normalize and reset css file
  * Shouldn't need to load fontawesome twice.
* See if you can use borders over hr tags
* Would use a form for the qualities and input to add a new quality
* Would keep all related items in one form
* Would recommend using a `figure` for this section. Typically a figure is an image, diagram, etc.
* Make sure html in your JS is formatted correctly as well.  Tabbing in lines correctly
  * Such as the `header` tag on line 159, and the closing `figure` tag on line 170.
* Good organization of styles
* Remember to alphbetize properties.  Won't dock you points on your score this time, but remember for your final project!
* Experiment more with using shorthand for styles like margins and borders
* Find places where you can group styles together such as `.searchterm` and `.btn-search-idea` or `.side-bar-button` and `.side-bar-label`
* Careful of using percentages for things like margins and paddings
  * Potentially could be the reason why the spacing in the sidebar shrinks as you squish the screen.
* Wouldn't recommend storing the starIcon image in the class (keep track of the boolean as you are doing in the star property, and then you can update the image based on that boolean on page refresh)
* Would move the findIndex functionality in deleteFromStorage back into the main.js where you are doing that similar functionality
* Shouldn't need to query downVoteButton, upVoteButton, starButton, etc in your global variables because they are dynamic elements (the cards are dynamic).  We will need to use `event delegation` for these.
* Should have an instantiation for every object, and use that instantiation's methods as opposed to one class handling all.
* Be consistent using function declarations in event listeners.
  * Wouldn't recommend ternaries if you won't be using the `else` in the conditional (aka ":")
* Keep working on how you can refactor updateTitle and updateBody into one function
  * Pseudo code: If `e.target` includes this class, pass an argument of "title" or "body" into one function.
  * Then use the paramater to do bracket notation so we can update the title/body 
* Shouldn't need to parse the local storage in every function
* Experiment using the closest method
* Would clean up commented out organization lines since it is pretty easy to tell where global variables, event listeners, and function declarations are

### Functional Expectations

*  Novice: Application meets all of the expectations of phase one.

### Comp Recreation

*  Advanced Beginner - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.). Transitions between screen sizes may not be smooth

### HTML - Style and Implementation

*  Advanced Beginner - Application adds to the above by using appropriate semantic elements and using `data-*` attributes for all data related things

### CSS - Style and Implementation

*  Advanced Beginner - Application adds organization for the whole stylesheet and within rules

### JAVASCRIPT - Style and Implementation

*  Advanced Beginner - Application adds to the above by correctly implementing a data model for the `Idea` class including all required methods