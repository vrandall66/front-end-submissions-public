## Student: Michael and Chase
## Evaluator: Pamela Lovett
## Notes/What To Work On:

### OVERALL
- YAY for making it through all the phases and doing a DTR!! Be sure to revisit the DTR as needed in future projects and that both partners touch all areas (HTML, CSS, JS) of the codebase

### DESIGN

- Some work to make it fully responsive - weirdness happening between different screen sizes. Add more than one media query to account for this.
- Ditch the alert for error messaging and find a more elegant solution. Tell the user to know that part of having a valid URL includes having `http://` tacked on the front
- Appreciate the `unread` counter - this was something that is often overlooked in the spec!!

### HTML
- YAY for running it through the screenreader and changing your code based on results!
- Read [this article](https://cantina.co/form-errors-screen-readers-can-access/) for information on using ARIA-LIVE to account for error-messaging with screenreaders
- Line 37 does not have the correct path to your local jquery doc

### CSS
- HOORAY for organizing CSS idiomatically!!
- Add `box-sizing: border-box` to override default box-sizing to make sure boxes are the exact width you set.
```css
  *, *:before, *:after {
    -webkit-box-sizing: border-box; 
    -moz-box-sizing: border-box; 
    box-sizing: border-box;
  }
```
- Avoid mixing named colors and hex codes in your CSS file - pick one and stay consistent

### JS
- For someone who doesn't know the backstory, it would be unclear as to why you are using jQuery selectors in some places but not overall. Stay consistent unless there is a reason. LOVE that you took a stab at doing this in vanilla JS
- Naming is pretty good on functions - could be improved on variables for created elements. The naming on these makes some of the lines hard to follow 
- Functionality is split up well!

### GIT/GITHUB
- Would like to see more branches in GitHub - should be working on branches for different features
- Be sure to stay consistent with commits. Be concise yet descriptive in your commit messages so that they are easy to navigate

## Functional Expectations

* Exceptional: You completed Phase Three and did something with Phase Four.

## COMP RECREATION / DESIGN

* Advanced Beginner  
* Proficient  

## HTML

* Proficient  

## CSS
 
* Advanced Beginner  
* Proficient   

## JS/jQuery

* Proficient  

## GIT & GITHUB

* Novice
* Advanced Beginner   

## Pairing/Collaboration
 
* Advanced Beginner  
* Proficient    