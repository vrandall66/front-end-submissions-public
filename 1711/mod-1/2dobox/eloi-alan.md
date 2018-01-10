## Students: Eloi & Alan
## Evaluator: Pamela Lovett
## Notes/What To Work On:

### DESIGN/COMP
- Completed through Phase 3. Very little refactoring of CSS - mostly JS.
- Code that was added to the project is not responsive. Weird things happening at different break points
- Partial filtering - must refresh screen to work properly
- Only need filtering for importance. For the future, be sure to clarify specs with instructors when unsure
- No visual indication of when the submit button is disabled/enabled

### HTML

- Nice job with labels and other ARIA attributes
- Be sure to run your app through a screen reader every time - main form does pretty well, but the dynamically generated cards are not fully accessible.

### CSS
- Good job organizing declarations within selectors alphabetically. Next time, try using [Idiomatic CSS](https://github.com/necolas/idiomatic-css) for organizing declarations

### JS
- Naming pretty easy to follow
- Be mindful of syntax. Follow [style guides for JS](https://github.com/turingschool-examples/javascript/tree/master/es5)
- Be ready to speak to all of your code - not just what you write, but also what you inherit
- Opportunities for refactoring for event handlers on filtering buttons by using delegation
- Unclear why you are pulling from local storage a second time in 50 - just append cards with `complete-task` as value to the page
- Remove leftover functionality in line 69
- Only pass in dynamic arguments in line 73 for constructor - `title`, `content`, `id`. `this.complete` property could be set up as boolean of true/false
- Pass entire object as argument to `createCard` in line 108 
- `downvote`/`upvote` quality could be refactored into one single function. Same with `editTitle`/`editContent`

### GIT/GITHUB
- Having one final push to master from one single commit is unnacceptable - be sure to make atomic commits, work on branches, etc

## Functional Expectations

* Advanced Beginner  
* Proficient  

## HTML

#### Accessibility

* Advanced Beginner  
* Proficient  

#### Style
 
* Proficient  

## CSS

#### Structure of Code

* Advanced Beginner  
* Proficient  

#### Implementation

* Advanced Beginner  
* Proficient    

## JAVASCRIPT

#### Data Types

* Advanced Beginner  
* Proficient  

#### Conditional Logic

* Proficient  

#### Functions & Scope

* Advanced Beginner  
* Proficient  

#### Arrays

* Advanced Beginner  
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

* Novice  

#### Github

* Novice  

## DESIGN

#### Design Concepts

* Advanced Beginner 

## PAIRING

#### Collaboration

* Advanced Beginner  
* Proficient  
