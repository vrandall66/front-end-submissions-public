## Student: Keila & Megan
## Evaluator: Pamela Lovett
## Notes/What To Work On:


### DESIGN/COMP
- Application is not responsive. Satisfies the basic functional expectations for the project. Quality does not persist.

### HTML
- Get rid of unnecessary spacing between lines
- Good job using labels - next time use  `aria-label` attribute on inputs instead of label elements (since you are not using a visible label)
- Nice job using landmark roles for ARIA. It would be more appropriate for the section that contains your inputs to be given the role of `form` (and be housed within a form) instead of the role of `banner`. See this [W3C link](https://www.w3.org/TR/wai-aria-practices/examples/landmarks/banner.html) for information on what is considered a banner.
- Inputs should have a form around them for accessibility w/keyboard. This allows you to submit with a keypress (as it's currently set up, it only submits on click)
 - Be sure to run your app through a screen reader every time - although the main form is okay, the dynamically generated cards are not accessible.

### CSS
- Nice work alphabetically organizing declarations within selectors
- Next time, try using [Idiomatic CSS](https://github.com/necolas/idiomatic-css) for organizing declarations
- Add `box-sizing: border-box` to override default box-sizing to make sure boxes are the exact width you set.
```css
  *, *:before, *:after {
    -webkit-box-sizing: border-box; 
    -moz-box-sizing: border-box; 
    box-sizing: border-box;
  }
```
- Use reset or normalize file to avoid declarations where you undo default styles (lines 6-8)
- Note that setting the `font-size` in px (line 2) runs into accessibility issues - as it will override any browser settings set by the user. Setting this to a percentage avoids this. 75% would be the equivalent of 12px. See [this](https://engageinteractive.co.uk/blog/em-vs-rem-vs-px) article for a more detailed explanation
- Be sure that your flex properties are doing what you want. You are using the `align-self` property in several places where it isn't actually doing anything to the layout


### JS
- Nice job speaking to your code!
- Be sure to use `var` before initializing your variable `i` in the loop on line 12
- You should not be instantiating new Cards when pulling from local storage like in line 15. One unique card object should be instantiated upon creation (line 24). That same unique object can be pulled from localStorage and appended to the page without calling `new`
- Be sure to remove any commented out code/broken functionality before submitting final product
- Nice work building prototype methods from `Card`!
- Put `qualityArray` (line 68) inside your constructor function so that every card has it's own quality array.

### GIT/GITHUB
- Be sure to follow conventions of capitalizing first letter in all commits. Be verbose and precise in your commit messages.
- Continue to name branches based on features that you are working on

## Functional Expectations

* Novice  Application meets all of the basic functional expectations of create, edit, delete, persist in local storage.

## HTML

## Accessibility

* Advanced Beginner Leverages more precise semantic tags when applicable, and employs basic ARIA roles attributes for added clarity in structure, descriptive image alt attributes, title attributes for applicable anchor tags.
* Proficient  Employs detailed accessibility practices throughout markup, especially in forms and can speak to decisions made in accessibility choices as it relates to specific accessibility concerns.

## Style

* Proficient  Crafts lean, efficient markup that is easy to read and follow across naming conventions, structure, and solid formatting that follows industry best practices.

## CSS

## Structure of Code

* Advanced Beginner Can cleanly and logically organize CSS rules according to similar categories (i.e. typography, layout, components), and then logically organize the remaining CSS rules based on flow of the markup. Organizes properties within rules alphabetically.

## Implementation

* Novice  Can articulate how the CSS box model works and apply it appropriately in a static layout.
* Advanced Beginner Can articulate the differences between the approaches of absolute/relative positioning, flex-box, floats, and can appropriately apply the approaches to solve a variety of layout problems.

## JAVASCRIPT

## Data Types

* Advanced Beginner Can diagnose when issues of data-type mismatch are present and appropriately redirect their coding and/or research efforts accordingly to solve the problem.
* Proficient  Can identify and track data types through any variety of functions, understanding their affect and result on each line of code. Knows which scenarios are better suited for objects vs. arrays and employs them accordingly.

## Conditional Logic

* Advanced Beginner Uses if/else statements, but there are multiple levels of nesting, which makes the paths through the code difficult to follow. Understands what is “truthy” and “falsey” in JavaScript.

## Functions & Scope

* Advanced Beginner Developer is comfortable using multiple arguments to pass data into functions. Understands how variables are scoped at the function level and global level. Functions are named descriptively. Knows when and why to use return in a function.
* Proficient  Functions have single responsibility. The entirety of the function is easy to read what functionality it contains. Function is generally shorter than 8 lines. Uses functions to eliminate repeated code. Comfortable refactoring any piece of code and extracting it to a function.

## Arrays

* Advanced Beginner Can modify arrays by adding or removing specific elements - uses array methods such as push or shift. Can use a for loop to iterate through array.

## Objects & Prototypes

* Proficient  Can use object prototypes. Can articulate the definition and the “why” of an object prototype - the best use cases for prototypes.

## DOM Manipulation

* Proficient  Able to extract information, modify attributes, or append/prepend data in the DOM easily regardless of whether they are employing vanilla JavaScript or jQuery. Understands how to harness event bubbling.

## Style

* Advanced Beginner Code shows strong effort toward organization, but suffers from long functions, unnecessary or poorly named variables, and requires significant refactoring. Application may have some duplication and minor bugs.
* Proficient  Code is logically organized, such that reader can easily follow the progression of the app because variable and function names are descriptive and follow a single responsibility approach. There are no major bugs and minimal duplication.

## GIT & GITHUB

## Git

* Advanced Beginner Can create branches and willingly attempts to incorporate branches into their workflow. Commits, while infrequent, are increased in volume and show improvements in description.
* Proficient  Commits changes frequently with detailed commit messages. Uses feature branches to keep master branch free of incomplete features or bugs.


## GitHub

* Advanced Beginner Can execute basic pull requests with context about changes in description. Can keep local and GitHub repositories in sync.

## DESIGN

## Comp Recreation

* Advanced Beginner Can accomplish about 50-75% of the large and small design details and can logically rework them on at least 1 breakpoint.

## PAIRING

## Collaboration

* Proficient  Can diplomatically handle issues that arise between the pair through respectful, focused, targeted feedback and implement changes to positively adapt the working relationship and keep the project on track. Can effectively implement tactics to support their partner’s learning and project goals, while also honoring their own personal learning and project goals, should the two be different or at different levels due to skill delta.
