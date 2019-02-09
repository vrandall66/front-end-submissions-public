## Student: Tiffany Bacher, Jon Keever
## Evaluator: Khalid Williams 
## Notes/What To Work On:

* Number of guesses doesn't reset each round
* Can't add another card after you clear all cards
* Remove all cards button is created too many times
* Should not be able to win the game if one guess is outside the possible range
* Don't forget SVG icon for all errors
    * In general, error handling should match the solution in the comp 

* The UI on the winning cards isn't quite right 
  * Take a look at the makeCard() function
* Need to get the app responding better on smaller screens (under ~510px)

* Good class naming on the HTML, structure is pretty clear and readable
* Nice use of semantic tags
* In future projects, don't leave commented out code in the HTML, even if it will be dynamically added to the DOM via JS
    * The github repo will look better if you take this out of the HTML file

*  CSS organized with main setions and then page flow 
* Formatting could be touched up
  * Alphabetize the properties
  * Keep multiple selectors on multiple lines
        * This would hold you back from a proficient

* JS 
  * Remove commented out code
  * DRY up your functions that are handling the same operation for multiple users via the use of parameters (ex: `updateResponseOne` vs `updateResponseTwo` and `compareGuessOne` vs `compareGuessTwo`)


### Functional Expectations

* __Advanced Beginner:__ Application meets all of the expectations of phase two.
.

------------------------------------------------------------------

### Comp Recreation

* __Novice:__ Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)

------------------------------------------------------------------

### HTML - Style and Implementation

* __Proficient:__ Application adds to the above with markup that is easy to read and follows across naming conventions


------------------------------------------------------------------

### CSS - Style and Implementation

* __Proficient:__ Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle and
  * Has 3 or less media queries for responsiveness

------------------------------------------------------------------

### JAVASCRIPT - Style and Implementation

* __Advanced Beginner:__ Displays good understanding of arguments vs parameters and:
  * Uses function declarations over anonymous functions in event listeners
  * Uses if/else statements to handle multiple paths of logic/error handling
