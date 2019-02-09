## Student: Menashe Borukhov, Ebenezer Ingalsbee
## Evaluator:
## Notes/What To Work On:

* Comp recreation looks good
* Responsive, but on small screens doesn't perfectly match the comp
    * Latest guess section needs to stack vertically on mobile 
    * Some of the transitions are a little awkward, breakpoints could come a bit earlier
        * Guess button text overflows a bit when screen is ~ 610 px 


* Adding winner cards has a few bugs
    * Names don't add themselves correctly when mutliple winners are on the page
* No functional error handling

* Don't have more than five selectors on a CSS rule
* Try not to micromanage the UI with so many small media queries in the future
* Keep your class names more descriptive (`card1` and `card2` don't explain much about the purpose of those cards)
* Include a normalize file!!

* Keep function names descriptive, but not redundant (don't need to have `Func` as part of a function name)
* Think of creative ways you can keep functions under 10 lines (ex `querySelectorAll` and for loop...)
* A few functions could be DRYed up by taking advantages of paramters and arguments; good place for refacrtoring
    * ex: `p1GuessEval` and `p2GuessEval`
* Use `===` instead of `==` (line 130)


### Functional Expectations

* __Novice:__ Application meets all of the expectations of phase one.


------------------------------------------------------------------

### Comp Recreation

* __Novice:__ Application implements all major comp details accurately and correctly on desktop only (colors, fonts, icons, spacing, alignment, etc.)


------------------------------------------------------------------

### HTML - Style and Implementation

* __Advanced Beginner:__ Application adds to the above with HTML that incorporates semantic HTML elements and has a simple, clean HTML structure.

------------------------------------------------------------------

### CSS - Style and Implementation

* __Advanced Beginner:__ Application adds organization for the whole stylesheet and within rules and
  * Has 5 or less media queries for responsiveness


------------------------------------------------------------------

### JAVASCRIPT - Style and Implementation

* __Advanced Beginner:__ Displays good understanding of arguments vs parameters and:
  * Uses function declarations over anonymous functions in event listeners
  * Uses if/else statements to handle multiple paths of logic/error handling
