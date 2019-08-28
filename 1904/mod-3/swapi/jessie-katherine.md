### Evaluator: Robbie
### Students: Jessie and Katie
### Comments:

* I like the overall theme, different from the generic star wars theme
* Is the right-panel scrolling text intentional - maybe needs some polishing, the zoomed-in text at the end is not readable
* The card and text is _very_ small on a high resolution screen, watch out for that
* It would be nice to have an indication on the card itself that it has been favorited, like a change in color of the heart or something
* What is the purpose of the star in the top-left corner of each card? Maybe just stylistic?

* I'm torn on the "Fetch" component naming. Usually components are named to represent physical things on the DOM and not actions
* Nice that you have a 404 page
* `checkLoading` seems to not be used yet, so I'm not seeing a spinner or anything to let me know the fetch is occurring but not yet finished
* Since these are all `li` elements, could you make this iterable and not hard code the `li`s? https://github.com/Jessiewithani/Swapi-Box/blob/master/src/components/CategoryCard/CategoryCard.js#L21-L31
* Do more with the fetch `catch` errors - something else other than `console.log` since the user will never see this or know what went wrong

* One failing snapshot test at time of review
* Great job getting some async tests in for API calls
* A couple linting errors/warnings remaining
* Good setting state tests in the Fetch component
* Overall, great job testing


## SwapiBox Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 
* 4 - Codebase has zero linter errors/warnings and README is well documented with images of different pages, setup, purpose of application, and group members. Project team uses a rebase workflow, taking advantage of github issues to track work.

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.

### Testing

* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.
* 4 - All async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).  Unit tests for snapshots and methods cover not only happy paths but also sad paths.  Evaluator has no recommendations for testing.