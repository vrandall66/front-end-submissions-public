## Student: Amy & Nyssa
## Evaluator: Pamela Lovett
## Notes/What To Work On:

- LOVE that you still pushed forward on specs even after the cutoff time for the project.
- Comp stays true to spirit of the comp - mobile needs to be tweaked.
- Good use of naming in branches and commits!
- Remove unnecessary spacing in HTML file. Good naming for classes. Incorporate more ARIA (lang, labels).
- Run through CSS selectors w/dev tools to be sure that every line is doing something - 10 declarations that aren't doing anything for the layout (mostly flexbox related)
- Good use of a counter to keep track of IDs on cards! Hooray for using $.each in line 27
- Opportunities for refactoring: Event listener from lines 50-95 should be refactored into single responsibility functions - too many things are happening here. Make title, body, and quality local variables. Should only need to pull value from input field (for creating object) one time. Once object is created, should only need to pass object as an argument instead of each individual property. 

## Functional Expectations

* Advanced Beginner Application allows for upvote/downvote and enables searching/filtering as defined in the spec

## HTML

### Accessibility

* Advanced Beginner Leverages more precise semantic tags when applicable, and employs basic ARIA roles attributes for added clarity in structure, descriptive image alt attributes, title attributes for applicable anchor tags.

### Style

* Proficient  Crafts lean, efficient markup that is easy to read and follow across naming conventions, structure, and solid formatting that follows industry best practices.

## CSS

### Structure of Code


* Advanced Beginner Can cleanly and logically organize CSS rules according to similar categories (i.e. typography, layout, components), and then logically organize the remaining CSS rules based on flow of the markup. Organizes properties within rules alphabetically.
* Proficient  Leverages cascading styles and CSS specificity rules to create more complex targeting of elements in order to reduce, reuse, share styles across elements. Organizes properties within rules based upon industry standard principles of writing consistent, idiomatic CSS.

### Implementation

* Advanced Beginner Can articulate the differences between the approaches of absolute/relative positioning, flex-box, floats, and can appropriately apply the approaches to solve a variety of layout problems.
* Proficient  Develops layouts that work cross-browser, are responsive, and can logically defend the choices made in implementation approach for layout.

## JAVASCRIPT

### Data Types

* Advanced Beginner Can diagnose when issues of data-type mismatch are present and appropriately redirect their coding and/or research efforts accordingly to solve the problem.
* Proficient  Can identify and track data types through any variety of functions, understanding their affect and result on each line of code. Knows which scenarios are better suited for objects vs. arrays and employs them accordingly.

### Conditional Logic

* Advanced Beginner Uses if/else statements, but there are multiple levels of nesting, which makes the paths through the code difficult to follow. Understands what is “truthy” and “falsey” in JavaScript.

### Functions & Scope

* Advanced Beginner Developer is comfortable using multiple arguments to pass data into functions. Understands how variables are scoped at the function level and global level. Functions are named descriptively. Knows when and why to use return in a function.
* Proficient  Functions have single responsibility. The entirety of the function is easy to read what functionality it contains. Function is generally shorter than 8 lines. Uses functions to eliminate repeated code. Comfortable refactoring any piece of code and extracting it to a function.

### Arrays

* Proficient  Does not use for loops for arrays - uses array prototypes, such as forEach, to iterate through or manipulate arrays. Can use array to store more complicated data structures such as objects or nested arrays. Is comfortable/efficient with reading array prototype documentation and can efficiently test/apply array prototype methods they have not worked with before.


### Objects & Prototypes

* Novice  Can declare an object literal and define/articulate properties vs. methods for an object. Can extract values of an object’s property, and assign new properties and/or reassign values of existing properties on an object.
* Advanced Beginner Can use object constructor functions and is comfortable with extracting values of properties on different object instances.

### DOM Manipulation

* Proficient  Able to extract information, modify attributes, or append/prepend data in the DOM easily regardless of whether they are employing vanilla JavaScript or jQuery. Understands how to harness event bubbling.

### Style

* Advanced Beginner Code shows strong effort toward organization, but suffers from long functions, unnecessary or poorly named variables, and requires significant refactoring. Application may have some duplication and minor bugs.
* Proficient  Code is logically organized, such that reader can easily follow the progression of the app because variable and function names are descriptive and follow a single responsibility approach. There are no major bugs and minimal duplication.

## GIT & GITHUB

### Git

* Proficient  Commits changes frequently with detailed commit messages. Uses feature branches to keep master branch free of incomplete features or bugs.

### GitHub

* Proficient  Is comfortable with resolving merge conflicts. Asks for review/merge of their pull requests from teammates. Is comfortable editing code based on review feedback from a pull request and resubmitting the branch code.

## DESIGN

### Comp Recreation


* Advanced Beginner Can accomplish about 50-75% of the large and small design details and can logically rework them on at least 1 breakpoint.
* Proficient  Developer captures the spirit and design intent of the comp. Some small details need polish to achieve a pixel-perfect match to the comp, but developer is clearly mindful of details and has made a conscious and careful effort to match the comp. Any design decisions left open to interpretation are handled thoughtfully and are well executed, but are more noticeable and/or unintuitive than they would be if the designer had provided the solution, or may not be totally seamless during screen-size transitions.

## PAIRING

### Collaboration

* Proficient  Can diplomatically handle issues that arise between the pair through respectful, focused, targeted feedback and implement changes to positively adapt the working relationship and keep the project on track. Can effectively implement tactics to support their partner’s learning and project goals, while also honoring their own personal learning and project goals, should the two be different or at different levels due to skill delta.