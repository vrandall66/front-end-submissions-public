## Student: Brandy Mello & Greg Anderson & Naomi Campos
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Good work on number of commits and number of branches.  (maybe could get broken out into a few more)
  * In general, good consistency on commit messages
  * Be care of very large commits
* Display message for if there are no ideas could be styled a bit better and potentially centered
* Make sure the app fills the entire window (especially when searching all cards)
  * Might see how we can center the cards a bit more
* Might have break point come in a little earlier
* Really good work keeping the HTML structure clean
* Cheers to using the BEM classes
* Alt tags can be more specific about what the image is describing.
* Great work adding alt tags and using for attributes on labels to hook up inputs
* Good organization of styles and alphabetizing the properties
* Would be careful of using decimals for ems
  * When honing in, try using pixels so it's easier to read and be more specific
* Be clear with names for grid areas
* Experiment with other ways you can target elements instead of using all classes
  * For example, if I wanted all the p tags in a section with a class of container, I could do `.container p` and write my styles
* In general good work with grouping up styles that share similar properties, be consistent throughout the media queries as well
* Might be a bit overkill using a variable for every single property in instantiateIdea function
  * Pass the propperties through as the values to each key inside of the object
* Instead of having to grab and update everything, update only the element that is being updated
* Might move some of the logic for the updateQuality into the method of the class
  * Data stuff handled in class and DOM stuff in main.js
* Logic where you are toggling the boolean for triggerStar could be handled in class

Pseudo Code for updating title, body, etc.

```js
var inputVal = e.target.value;
if (e.target.className === "title") {
  idea.UpdateIdea('title', inputVal)
}

updateIdea(key, value) {
  this[key] = value
}
```

### Functional Expectations

*  Advanced Beginner: Application meets all of the expectations of phase two.

### Comp Recreation

*  Advanced Beginner - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.). Transitions between screen sizes may not be smooth

### HTML - Style and Implementation

*  Proficient - Applications adds to the above with markup that is easy to read and follow across naming conventions

### CSS - Style and Implementation

*  Proficient - Applications adds to the above by removing repetitive rules and blocks of code according to the DRY principle

### JAVASCRIPT - Style and Implementation

*  Proficient - Application adds readability by incorporating both DRY and SRP practices and students can speak to implementation decisions and:
  *  Uses event delegation correctly on dynamic elements for deleting, editing, & starring an idea
  *  All functions are less than 10 lines
  *  There are no global variables aside from query selectors and two arrays for your ideas and qualities
  *  There are no nested if else statements