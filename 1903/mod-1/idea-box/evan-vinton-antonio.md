## Student: Evan Markowitz & Vinton Te'o & Antonio Fry
## Evaluator: Travis Rollins
## Notes/What To Work On:
* Great number of commits, and good number of branches
* Be consistent with kabob case on branch names
* Good use of imperative tense and being descript on commits
* Several bugs with the user experience
  * A few bugs with  starring ideas (star card 2, card 1 is starred on refresh, show starred button doesn't work unless I click on qualities first, etc.)
  * Would remove the border from the active state on each quality
    * Color of qualities on the side bar don't match the comp
  * Inputs do not clear out after saving.
  * Only first two cards save it seems?  If I create multiple, only the first 2 save.
  * Can keep updating the quality past genius to an empty quality
* Wouldn't recommend having a card being displayed from the beginning unless it is a card saved by the user.
* Width of inputs could take utilize more space when it's 900px and lower
* Add New Quality button is still showing on mobile view even if menu is not open
* Missing the overlay in the mobile view when I open up the menu
* Careful not to use inline styles, see how you can do it with classes
* Remember to inclue a normalize or reset stylesheet
* Remember to also clean up commented out lines
* Make sure the label connects with the input for accessibility reasons
* A few too many forms.  Could have all things related to qualities be included in one form.  Don't think we need a form for the `Show Starred Ideas` since this is just a button, but no information is being required and sent anywhere. 
* Might use ids over classes for javascript reasons on inputs, buttons, form related things
* I would remove the card that is displayed at the very beginning.  Leave text to let the user know if there is no cards, but avoid the flicker of the card changing really quickly on page load.  This will clean up your HTML as well.
* Good organization of styles
* Remember to alphabetize the properties of each style.  I won't dock your score down this time, but make sure you remember this for the final project.
* Remember box-sizing: border-box.  It will definitely help keep heights/widths the way you expect them too.
* See how you can use shortcuts of styles like margin, border, etc.
* Some places where we can group more styles together
* Also some styles could get cleaned up that aren't being used (z-index: -10 on header, )
* Stay away from using text-align on containers
* Remember semi colons at the end of lines.  Some lines are breaking because you are missing this.
  * Also repeated line of margin-bottom. (looking at `.quality-button-form`)
* Instead of using display block on a number of elements to get them to stack on top of each other in the media query, see how you can use flex direction to get them to behave the way you want
* See how you could refactor the starred property in the idea class in the updateIdeaQuality method
  * Might move where the starred property is being updated into the updateIdea method
* Careful of nested conditionals in the updateQuality method (would recommend moving some of the conditional logic including which className it is back into the main.js)
* See how you can update the editIdeas using bracket notation
* Should remove extra global variables in the idea.js file
* Good organization of Javascript with global variables, event listeners, and function declarations
* Good use of event delegation on the deleting functionality
* applyStar function seems a bit repetitive.  
  Could I include that conditional in the saveNewIdea function and update the img based on if obj.starred is true or not?
* How could we refactor line 246 in qualityRetrieve?
  * We're not using the if conditional, only the else. 
* Noticed in order to filter through, things are being either display `block` or `none`.  Interestingly, these do not remove the element. (check your dev tools and you will still notice the element there even if it is display: none)
  * This means we still have to search and filter through those elements.  See how you can `remove` them.
  * Potentially instead of iterating through the DOM, we can iterate through just our ideas array, filter out what we don't want, clear the DOM, and reappend the cards we want).
* Think about how toggleButtonColor can be refactored.
  * Maybe we loop through the all of the qualities, zero them out in a function, then update the class on the event.target

### Functional Expectations

*  Advanced Beginner: Application meets all of the expectations of phase two.

### Comp Recreation

*  Advanced Beginner - Application implements all major comp details accurately and correctly on desktop and mobile (colors, fonts, icons,spacing, alignment,  etc.). Transitions between screen sizes may not be smooth

### HTML - Style and Implementation

*  Advanced Beginner - Application adds to the above by using appropriate semantic elements and using `data-*` attributes for all data related things

### CSS - Style and Implementation

*  Advanced Beginner - Application adds organization for the whole stylesheet and within rules

### JAVASCRIPT - Style and Implementation

*  Advanced Beginner - Application adds to the above by correctly implementing a data model for the `Idea` class including all required methods