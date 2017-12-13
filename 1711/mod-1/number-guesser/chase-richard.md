## Student: Chase Richard
## Evaluator: David Whitaker
## Notes/What To Work On:

### html
* Continue to use aria-label on all inputs
* Limit number of empty lines in html

### css
* Comment up different sections for better organization

### js 
* Pull function declarations outside of the event listener
* Keep conditionals inside of functions, as is they are living in the global space
* Try organizing differently by having all global vars at the top, then event listeners, and then functions
* Some variable declarations are being used as functions ie.

```javascript
  this:
  var lastGuessError = document.querySelector("#lastGuessWas").innerText = "Please enter a number between 1-100";
   
  should be:
  function lastGuessError() {
    document.querySelector("#lastGuessWas").innerText = "Please enter a number between 1-100";  
  }
```

* Global vars should be return value of querySelector function

## Functional Expectations

* Advanced Beginner: Application meets all of the expectations of phase two.  


## COMP RECREATION / DESIGN

* Advanced Beginner  


## HTML

* Advanced Beginner  


## CSS

* Advanced Beginner  
* Proficient  


## JS/jQuery

* Advanced Beginner  

