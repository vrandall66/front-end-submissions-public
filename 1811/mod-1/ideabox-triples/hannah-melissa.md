## Student: Hannah Hyde, Melissa LaChasse
## Evaluator: Khalid Williams 
## Notes/What To Work On:

#### General
* Github looks good, lots of commits and feature branches
    * Keep the commit messages in the active tense
* Local storage saving looks good
* Quality changing isn't working
* No show more and show less
* Editing is working on the DOM but not updating in localStorage
* Resposiveness:
    * Transitions look good, but the search bar overlays the styling dividers on small screens
        * This is the main thing holding you back from advanced beginner on Comp Recreation

#### HTML:
* Don't forget to delete the commented out HTML
    * This is the main thing keeping you at a novice; otherwise, the html is at advanced beginner
* Data attributes in the JS HTML that's generated
* Try using the `for` attribute for your input labels to make things more accessible

#### CSS:
* Clean up the empty rules and commented out properties
* Alphabetize the properties within the rules
* Make sure you can justify why you're adding a max screen size for your largest media query

#### JS:
* IDEA
    * Everything but changeQuality is working
    * The default value for the `idea.quality` is not being utilized
    
* MAIN
    * There are a few console logs you could clear out
    * The deleteIdea function is a bit unclear, but it's a fine way to do it
        * If you used a data attribute or had a way to access the instance's id from the DOM instance, then you should be able to access the correct instance in your `arrayOfIdeas` array. This would be a potential solution without making a new dummy instance with the same id.
    * A data-attribute could help more easily grab and edit the quality associated with a particular DOM instance of an idea

### Functional Expectations

* [ x ]  Novice - Application meets all of the basic functional expectations of create, edit, delete, and those changes persist in `localStorage`


------------------------------------------------------------------

### Comp Recreation

* [ x ]  Novice - Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)


------------------------------------------------------------------

### HTML - Style and Implementation

* [ x ]  Novice - Crafts markup according to the [turing html style guide](https://github.com/turingschool-examples/html)
* [ ]  Advanced Beginner - Application adds to the above by using appropriate semantic elements and using `data-*` attributes for all data related things

------------------------------------------------------------------

### CSS - Style and Implementation

* [ x ]  Novice - Crafts CSS according to the [turing css style guide](https://github.com/turingschool-examples/css)


------------------------------------------------------------------

### JAVASCRIPT - Style and Implementation

* [ x ]  Advanced Beginner - Application adds to the above by correctly implementing a data model for the `Idea` class including all required methods
