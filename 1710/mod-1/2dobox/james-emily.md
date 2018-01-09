## Student: James & Emily
## Evaluator: Pamela Lovett
## Notes/What To Work On:

- Clean design. Stays true to the comp. Fully responsive. Additional functionality (importance levels buttons) fits well with the original comp. Be sure that importance rating is aligned with up/down vote buttons. Move 'Show More' button to bottom
- Happy to hear that pairing went well. YAY for doing a DTR!!! Cool to hear that you were whiteboarding as part of the process.
- Love that you are using Waffle. Good naming on commits/branches.
- Good use of semantic elements in HTML and ARIA! Good spacing/indentation. 
- Be sure that your attribute is 'aria-label' on your inputs - not just 'label.' Include ARIA in the HTML you dynamically add with JS. Next time, use a screenreader to go through the page. The dynamically added cards are mostly unreadable by the screenreader. The contrast on the filter buttons is not sufficient, per accessibility testing. 
- CSS could use clean up. Was able to remove over 20 declarations that were unused/not doing anything. Review cascading stylesheets and inheritance. Be sure to not assign values of display or inline on elements that are that by default. Outline-style is none by default.
- Overall, JS file looks pretty good. Most functions are single responsibility. Like that there is a single function for edit title/task as well as filtering for importance. Nice use of array prototypes!
Areas for refactoring below:

- Unclear why you are pulling from storage again in lines 75 and 150  - already looping over an array that includes cards you've pulled from storage.
- Unused parameter of 'importance' in Line 175.

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

* Proficient  
* Exceptional  

#### Arrays

* Advanced Beginner
* Proficient    

#### Objects & Prototypes

* Proficient  

#### DOM Manipulation

* Proficient

#### Style

* Proficient
* Exceptional

## GIT & GITHUB

#### Git

* Proficient  

#### Github
 
* Proficient  
* Exceptional  

## DESIGN

#### Design Concepts

* Proficient    

## PAIRING

#### Collaboration
 
* Proficient  
* Exceptional
