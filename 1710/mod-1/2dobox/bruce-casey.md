## Student: Bruce & Casey
## Evaluator: Pamela Lovett
## Notes/What To Work On:

- Design is pretty accurate. Fully responsive. Move 'show more' button down to bottom or make it obvious to the user that more cards have been added off-screen.
- Add indication on hover that buttons are clickable. Text on the buttons themselves is kind of large. 
- YAY for completing 2/3 of the extensions!
- Be sure to have a DTR next time. Glad to hear that pairing went well without having one in place.
- Good naming on commits/branches.
- Good use of semantic elements in HTML and ARIA! Good spacing/indentation. And HOORAY for forms!!!
- Add lang attribute to HTML. Be sure to add ARIA to dynamically rendered HTML in JS file.
- Next time, use a screenreader to go through the page. The dynamically added cards are mostly unreadable by the screenreader. The contrast on the filter buttons is not sufficient, per accessibility testing. 
- CSS could use a quick pass for refactor. Just under 20 declarations that were unused/not doing anything. Review cascading stylesheets and inheritance. Outline-style is none by default.
- JS file is pretty good overall. Easy to follow logic and code is pretty readable. Nice use of array prototypes in some functionality! Very little redundancy - love how you combined functionality for editing title/task and changing importance.
Areas for refactoring below:

- Lines 18-22 could be refactored into single event listener by passing in $(this).text() as argument instead of hardcoded string (being sure to adjust for case-sensitivity).
- Unnecessary parameters placed (importance and completed) in line 74.

## Functional Expectations

* Proficient  
* Exceptional  

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

## DESIGN

#### Design Concepts

* Proficient  

## PAIRING

#### Collaboration

* Proficient  