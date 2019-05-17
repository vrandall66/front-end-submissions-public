## Student: Naomi Campos and Jessie Le-Ho
## Evaluator: Khalid Williams 
## Notes/What To Work On:

__General__
* Github struggles 
  * Merge conflicrs were a pretty consistent issue
    * Make sure to avoid this in the future by only merging into master when doing a PR -- you should be solving merge conflicts after you pull down master and try to merge those changes into local feature branches
  * Actual commits looked good 
* In the readme, make sure to leave a space between your hashmarks and text in order to make heading 
  * `# Number Guesser`, not `#Number Guesser`
* __Make sure to put a link to your live site in the readme as well__ 

__Functional Notes__ 
* Buttons disabled when fields are not populated
* Cards adding to the page 


__Comp Recreation__ 
* Repsonsiveness is a bit of an issue
  * Need to make sure you're setting your flex properties on the right elements (flex containers vs flex items)
* Some issues with attention to detail for comp recreation
  * Missing lines on the subtitle
  *  

__HTML__
* Semantic HTML 
* Using divs for a lot of buttton grouping, but using semantic tags within that 
* Potentially over-used classes 
* Don't forget to remove commented out code, even if the comments refer to a template of what will be added. If it's not on the DOM at page load, it doesn't need to be there
* The HTML was on the line between novice and advanced beginner. You had a good structure, but didn't fully leverage the differences between classes and ids for your styling.
  * The legend tag should not be used without a fieldset. An h4 or other heading tag would have been a more appropriate choice 
  * It's awesome that you were enthusiastic about using semantic tags, just make sure you can justify all your choices 

__CSS__
* Following the page flow for organization 
* Redundant class naming 
  * All of your input-boxes could have had one `input-box` class, then their own unique ids for query selecting
* Make sure you're closing all your rules (line 85)
* Make sure to be consistent with your semicolons and spacing (line 137)

__JS__ 
* Make sure you can both articulate how all of the code is working 
* You could use a for loop to dry up your series of event listeners on lines 37 - 54
* Take out commented code and console.logs  
* Can dry up your `gamePLay` functions as well 
* Can use a for loop and querySelectorAll to shorten your `resetGame` function
  * Think about how many elements you're setting the `value = ''` for

### Functional Expectations

* __Novice:__ Application meets all of the expectations of phase one.
* Advanced Beginner: Application meets all of the expectations of phase two.
* Proficient: Application meets all of the expectations of phase three.
* Exceptional: Application adds three or more of the extensions from phase four.

------------------------------------------------------------------

### Comp Recreation

* __Novice:__ Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)
* Advanced Beginner: Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.). Transitions between screen sizes may not be smooth.
* Proficient: Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements added generally match the visuals established in the comps, but may be slightly awkward.
* Exceptional: Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons, spacing, alignment,  etc.) with smooth transitions between screen sizes. Additional elements that have been added match the visuals established in the comps.

------------------------------------------------------------------

### HTML - Style and Implementation

* Novice: Crafts markup according to the [turing html style guide](https://github.com/turingschool-examples/html)
* __Advanced Beginner:__ Application adds to the above with HTML that incorporates semantic HTML elements and has a simple, clean HTML structure.
* Proficient: Application adds to the above with markup that is easy to read and follows across naming conventions
* Exceptional: Application adds to the above by using [BEM](http://getbem.com/), [SMACCS](https://smacss.com/), or another set of naming conventions for classes and:
    * Implements html that is accessible for folks with visual disabilities. Reference [this lesson plan](http://frontend.turing.io/lessons/floating/web-accessibility.html)

------------------------------------------------------------------

### CSS - Style and Implementation

* Novice: Crafts CSS according to the [turing css style guide](https://github.com/turingschool-examples/css)
* __Advanced Beginner:__ Application adds organization for the whole stylesheet and within rules and
  * Has 5 or less media queries for responsiveness
* Proficient: Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle and
  * Has 3 or less media queries for responsiveness
* Exceptional: Application adds to the above by using [BEM](http://getbem.com/), [SMACCS](https://smacss.com/), or another set of naming conventions for classes

------------------------------------------------------------------

### JAVASCRIPT - Style and Implementation

* Novice: Crafts JS according to the [turing js style guide](https://github.com/turingschool-examples/javascript/tree/master/es5)
* __Advanced Beginner:__ Displays good understanding of arguments vs parameters and:
  * Uses function declarations over anonymous functions in event listeners
  * Uses if/else statements to handle multiple paths of logic/error handling
* Proficient: Application uses event delegation correctly on dynamic elements and:
  * Keeps functions DRY with a focus on SRP and can call functions within functions
  * There are no nested if/else statements
*  Exceptional: Functions and code are well-refactored and show developer empathy and:
  * No global variables aside from query selectors, min & max, number of guesses, and start time
  * All functions are less than 10 lines
  * Uses logical operators instead of if/else statements where applicable