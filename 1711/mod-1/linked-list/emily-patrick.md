## Student: Emily and Patrick
## Evaluator: Pamela Lovett
## Notes/What To Work On:

### OVERVIEW
- All the way through Phase 4!!! You both did great with speaking to your code.

### DESIGN
- Stays true to the spirit of the comp 
- Like the color choices for the counter
- Add spacing between borders and cards. Make sure that the 'Linked List' header is flush with inputs/buttons
- Some work to make it fully responsive - weirdness happening before different media queries
- Ditch the alert for error messaging and find a more elegant solution. Tell the user to know that part of having a valid URL includes having `http://` tacked on the front
- Bookmark box falling outside of parent container

### HTML
- Good spacing. Keep using semantic tags.
- Lines 3-39 should be indented two more spaces. Lines 7 & 8 should be one line. Use [HTML Style Guide](https://github.com/turingschool-examples/html) for reference
- Add aria-labels to inputs and send through screen reader
- Inputs should have a form around them for accessibility w/keyboard. This allows you to submit with a `keypress` (as it's currently set up, it only submits on `click`)

### CSS

- Nice job with organizing declarations alphabetically in each selector
- No need for a 0 margin on body since you are using a reset 
- Overuse of absolute positioning. Typically, you want to use absolute ONLY when you can't get any other positioning to make the layout work
- Add `box-sizing: border-box` to override default box-sizing to make sure boxes are the exact width you set.
```css
  *, *:before, *:after {
    -webkit-box-sizing: border-box; 
    -moz-box-sizing: border-box; 
    box-sizing: border-box;
  }
```

### JS
- Nice job using named functions in event listeners
- Unclear why event listener is set up on body instead of the link counter div in Line 6
- Like the focus back to the input on 15 and 22
- Check for using soft wrap on long lines of code
- Nice job knowing what `this` is in your code!! As well as being able to speak to your regex code!
- Opportunity for some refactoring in event listener for creating card - but good overall! 

### GIT/GITHUB
- HOORAY for Waffle!!! Happy to see that it helped with driving the project
- Nice work using branches to work on features. Be sure that you are following conventions for commiting - capitalize first letter and be concise and specific with commit messages

## Functional Expectations

* Exceptional: You completed Phase Three and did something with Phase Four.

## COMP RECREATION / DESIGN

* Advanced Beginner  
* Proficient  

## HTML

* Advanced Beginner  

## CSS

* Advanced Beginner  
* Proficient  

## JS/jQuery
 
* Proficient  

## GIT & GITHUB
 
* Proficient 

## Pairing/Collaboration

* Proficient  