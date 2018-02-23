## Students: Matt & Patrick
## Evaluator: Pamela Lovett
## Notes/What To Work On:

### DESIGN/COMP
- PUMPED that you decided to tackle working with time and using the MomentJS library
- Like the changes you made so that `Show More ToDos` button only appears when there are more than 10 todos
- Not sure about that gradient - but other colors work together
- Redesign the `Completed Task` button so that it looks like a button. No indication that is a button or clickable
- Like that you worked in the ability to filter for more than one importance type

### HTML

- Nice job with labels and other ARIA attributes - especially the use of landmark roles
- Be sure to run your app through a screen reader every time - main form does pretty ok... checkboxes for filtering do well... but the dynamically generated cards are not fully accessible.

### CSS

- Set font-size on your html selector. Also note that setting the `font-size` in px (line 9) runs into accessibility issues - as it will override any browser settings set by the user. Setting this to a percentage avoids this. 62.5% would be the equivalent of 10px. See [this](https://engageinteractive.co.uk/blog/em-vs-rem-vs-px) article for a more detailed explanation

### JS

- Good refactoring of event listeners to named functions
- Continue to work on naming. Good work with being more verbose but some naming still makes the code hard to follow - like  `cardAppendAdjust`, `cardAdjust`, and `timeIfElse`. It is not clear what these functions do based on names
- Unclear why classes are being passed around in JS that are controlling CSS. Use add/remove/toggle for CSS classes when necessary 
- In line 116 (and elsewhere) use boolean instead of 0 vs 1 for `completed` vs `non-completed`
- Importance array can be saved/accessed directly in constructor function instead of created and returned from function
- Opportunities for refactoring with append/prepend as well as other functionality around voting, importance, title/task
- Great work getting things refactored from inherited repo, overall                                                                     


### GIT/GITHUB
- Be sure to name branches/PRs descriptively - for features
- Stay consistent in being verbose/concise with commits

## Functional Expectations

* Exceptional  

## HTML

#### Accessibility

* Advanced Beginner  
* Proficient  

#### Style

* Proficient  

## CSS

#### Structure of Code

* Proficient  

#### Implementation
 
* Proficient  

## JAVASCRIPT

#### Data Types
 
* Proficient    

#### Conditional Logic

* Proficient  

#### Functions & Scope
 
* Proficient  

#### Arrays
 
* Proficient  

#### Objects & Prototypes

* Advanced Beginner  
* Proficient  

#### DOM Manipulation

* Proficient  

#### Style

* Advanced Beginner
* Proficient  


## GIT & GITHUB

#### Git

* Proficient  

#### Github

* Proficient  

## DESIGN

#### Design Concepts

* Proficient  

## PAIRING

#### Collaboration
  
* Proficient
* Exceptional
