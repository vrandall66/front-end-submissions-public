## Student: Amanda & Michelle
## Evaluator: Pamela Lovett
## Notes/What To Work On:

- Comp is pretty spot on and stays true to original design. Comp is fully responsive. Minor details to be adjusted - mainly shrinking size of Completed button on mobile view. Opportunities for UX while hovering over buttons. It is not clear that filter buttons are buttons with current design choices.
- Good naming on commits/branches.
- YAY for using DTR! Glad to hear that there was good communication happening during project.
- Good use of semantic elements in HTML and ARIA! Good spacing/indentation. 
- Be sure to use semantic elements/ARIA for HTML rendered in JS file as well. Next time, use a screenreader to go through the page. The dynamically added cards are mostly unreadable by the screenreader. The contrast on the text of your filter buttons is not sufficient, per accessibility testing. 
- CSS could use clean up. Was able to remove almost 30 declarations that were unused/not doing anything. Review cascading stylesheets and inheritance. Be sure to not assign values of display or inline on elements that are that by default. Outline-style is none by default.
- Overall, JS file looks pretty good. It's pretty readable and easy to follow your logic. Naming is good and most functions are single responsibility. Nice use of array prototypes!
Areas for refactoring below:

- Unnecessary variable assigned on line 59. Just pass in Date.now() in line 60.
- Unnecessary variables assigned on lines 82-83... though it can be argued that it improves readability VERY slightly. Could just pull values directly in condition in line 84.
- prevCarriageReturnTitle & Body can be refactored into single function.
- updateBody & updateTitle can be refactored into single function.
- upvoteQuality & downvoteQuality can be refactored into single function.

## Functional Expectations
 
* Proficient  

## HTML

#### Accessibility

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