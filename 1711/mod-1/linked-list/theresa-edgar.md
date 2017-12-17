## Student: Theresa and Edgar
## Evaluator: Pamela Lovett
## Notes/What To Work On:

### OVERVIEW
- YAY for making it through all of Phase III and most of IV! Nice work doing a DTR and checking in w/your partner. Love that you are placing learning as a priority.

### DESIGN
- Error messaging should have more direct instructions for avoiding the error
- Knock the red down on your clear read buttons, fix spacing between inputs 
- Hard to read the `read bookmarks` text on the screen

### HTML
- Lines 3-25 should be indented two more spaces to align with [HTML Style Guide](https://github.com/turingschool-examples/html)
- Like that you are using aria-required and lang attributes! Add labels to your inputs.

### CSS
- Good commenting for organization in CSS
- Use ems or rems for font sizes - don't rely on pixel density with so many user devices out there now
- Add `box-sizing: border-box` to override default box-sizing to make sure boxes are the exact width you set.
```css
  *, *:before, *:after {
    -webkit-box-sizing: border-box; 
    -moz-box-sizing: border-box; 
    box-sizing: border-box;
  }
```
- Use `background-color` not `background` to set the color for sections (Lines 6, 31, 40, 71, 78, 83, 87, 91) Don't mix color names and hex codes in your CSS file - pick one and stay consistent
- Avoid the use of IDs as CSS selectors to avoid specificity issues when your codebase grows
- Use reset or normalize file to avoid declarations where you undo default styles

### JS

- Like that you are using named functions for event listeners
- Opportunities for refactoring in JS: break apart bookmarkCreate
- Hooray for knowing what `this` is within your toggleRead
- Work on naming conventions. Some parts of the code are hard to follow due to naming

### GIT/GITHUB
- Like that you are commenting on your PRs. Nice use of branches to separate features.
- Work on being concise and descriptive in naming for commits

## Functional Expectations
(Link for url does not redirect and URL validation is not working)
* Proficient: Application meets all of the functional expectations in Phase Three.

## COMP RECREATION / DESIGN
 
* Advanced Beginner  
* Proficient  

## HTML

* Advanced Beginner  

## CSS

* Advanced Beginner    

## JS/jQuery
  
* Advanced Beginner  
* Proficient  

## GIT & GITHUB

* Advanced Beginner  
* Proficient   

## Pairing/Collaboration
 
* Proficient  
