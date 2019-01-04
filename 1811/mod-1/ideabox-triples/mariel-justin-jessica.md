## Student: Mariel, Justin Pyktel, Jessica Hansen
## Evaluator: Khalid Williams 
## Notes/What To Work On:

#### General
* Look back at the issue with the sorting button
* Good comp recreation on the whole
* Additions match the comp
    * Watch the alignment on the filter buttons (keep a uniform width with the page)
    * Be careful about keeping the filter buttons consistent in your media queries -- things were getting a little jumpy
* reloading page doens't call the hidden card function, but it does work on click or on save (new card) 
    * This is the main thing keeping you from proficient in functionality 
* Deleting the card works
* Quality searching is happening using filter in a forEach and searching for the srtring itself
* Responsiveness:
    * Show more button isn't reponsive due to time issues this morning
    * A few jumpy tranistions, no stacking in the filter cards buttons
* Good job keeping things persisting in localStorage

#### HTML:
* Nice job using naming conventions for the classes and ids
    * The intent with the conventions was good, but there are some areas with the naming is a little inconsistent (header section lines 12-20)
    * Take some more time to look into the deatails and philosophy of BEM, try and use their specific terminology; good job getting into the naming convention mindset though!
* Pretty semantic markup 
* Think of areas where you can make things more semantic (like the form at the top)
* You're misusing the `for` attribute for your input labels; they should correspond to the `id` attributes for your input, not the `name` attribute (it's a little bit different with radio buttons though)

#### CSS:
* Good organization, think about some areas where you can dry things up by finding a class to connect multiple elements (when you're using > 4 selectors)
* Try and have fewer media queries and consolidating some of your rules; fewer will keep things less jumpy

#### JS:
* Take a look back at the event delegation on the card field area
* Some functions are a little long, but seems prety dry on the whole
* Figure out a way to dry up the filter buttons
    * The conditional seems unnecessary in the filtering functions 

### Functional Expectations

* [ x ]  Advanced Beginner - Application adds 'Changing the quality of an idea' and enables 'Filtering and Searching by Text' as defined in the spec


------------------------------------------------------------------

### Comp Recreation

* [ x ]  Advanced Beginner - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.). **Transitions between screen sizes may not be smooth**



------------------------------------------------------------------

### HTML - Style and Implementation

* [ x ]  Novice - Crafts markup according to the [turing html style guide](https://github.com/turingschool-examples/html)

    * The main thing holding you back from advanced beginner is not utolizing data attributes. Overwise, the html was quite good.


------------------------------------------------------------------

### CSS - Style and Implementation


* [ x ]  Proficient - Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle


------------------------------------------------------------------

### JAVASCRIPT - Style and Implementation

* [ ]  Novice - Crafts JS according to the [turing js style guide](https://github.com/turingschool-examples/javascript/tree/master/es5)
* [ ]  Advanced Beginner - Application adds to the above by correctly implementing a data model for the `Idea` class including all required methods


