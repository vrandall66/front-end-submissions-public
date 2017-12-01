## Student: Melena & Sabrina
## Evaluator: Pamela Lovett
## Notes/What To Work On:

- Stays true to the spirit of the comp. Good color palette!! Fully responsive. 
- Add indication on hover that buttons are clickable. Filter buttons could be a little bigger. Move 'show more' button down to bottom or make it obvious to the user that more cards have been added off-screen.
- Good naming on commits/branches.
- Great job using a DTR. Sounds like things went well and that you both enjoyed doing all parts of the project together.
- Good use of semantic elements in HTML and ARIA! Good indentation. Remove unnecessary spacing between lines.
- Add lang attribute to HTML. Add label to search input. Be sure to use ARIA on HTML you render in your JS file. Use a screenreader to go through the page. The dynamically added cards are mostly unreadable by the screenreader.
- CSS could use clean up. Was able to remove over 30 declarations that were unused/not doing anything. Review cascading stylesheets and inheritance. Be sure to not assign values of display or inline on elements that are that by default. Outline-style is none by default.
- JS file good overall. Most functions are single responsibility. Hooray for dynamic functions for edit title/task and changing importance!
Areas for refactoring below:

- Group event listeners that are a single line together - for improved readability.
- Avoid names like instantiateNewObject for your functions. Confusing. Gives no clue as to what this object does.
- textValidation function isn't fully functional. Allows user to append empty cards with no title AND no input to DOM/save in storage. Still saves cards/appends even when one field is missing.
- Search funtionality broken.

## Functional Expectations

* Advanced Beginner
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

#### Arrays

* Advanced Beginner  
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

* Proficient 

## PAIRING

#### Collaboration
 
* Proficient  