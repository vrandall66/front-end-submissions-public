## Students: Hannah & Om
## Evaluator: Pamela Lovett
## Notes/What To Work On:

### DESIGN/COMP

- Made it through the middle of Phase 3 with strikethrough persisting! 
- Colors work together; however, cork background is kind of busy and distracting
- Be sure to test for edge cases - when more text is entered for `task` section, words overflow from card
- Use round button with checkbox for `Task Completed` to align with other buttons on card
- No visual indication of when the submit button is disabled/enabled

### HTML
- Good job using labels - next time use  `aria-label` attribute on inputs instead of label elements (since you are not using a visible label)
- Be sure to run your app through a screen reader  - although the main form is okay, the dynamically generated cards are not accessible.
- Path for jquery file is not correct in line 40

### CSS

- Nice work updating the media queries in CSS
- Love the `#555555` hex code - 55555555555
- Good job organizing declarations within selectors alphabetically. Next time, try using [Idiomatic CSS](https://github.com/necolas/idiomatic-css) for organizing declarations
- Continue to use console for debugging/checking to see that declarations are doing something

### JS
- Nice work with using named functions for event handlers
- What default behavior are you preventing in line 13?
- Easy to follow/read the code. Functions are single responsibility
- Some naming could be adjusted for clarity - `showTask`
- Unused var in line 83 - jus return the `retrievedKey` that has been parsed. No need to save it in a variable to return:
```js
return JSON.parse(retrievedKey);
```
- Opportunites for refactoring with `editTitle`/`editTask` using `.find()`

### GIT/GITHUB
- Should be more commits for features completed
- Remember to be consistently verbose in commit messages

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
 
* Proficient  

#### DOM Manipulation

* Proficient  

#### Style

* Proficient  

## GIT & GITHUB

#### Git

* Proficient  
 
#### Github

* Proficient  

## DESIGN

#### Design Concepts

* Advanced Beginner  
* Proficient  

## PAIRING

#### Collaboration

* Proficient  
