### Evaluator: Robbie
### Students: Amy and Kate
### Comments:

* The opening screen is great! Love the cartoon animation and the overall look of the page
* The form text on the opening page is getting very small
* The movie characters page needs some work - the scrolling text is going over the full page, and the favorite button is overhanging the character cards
* Would like a visual cue that a character is favorited, like the color of the Favorite button changes or something
* Bug: After singing out, all of the signed-in information is below the fold...
* I like the signed-in info off to the side - frees up a lot of vertical space. How would you handle this on mobile?

* Routes look good and make sense!
* Nice work using proptypes in your components
* For the `MovieCard` within the `MoviesContainer`, use something other than the index `key={i}`, if the index for some reason changes, then it is no longer unique and ties to that card - does the movie data have anything unique associated with it that could be used as a key instead?
* Interesting to see reuse of the `CharactersContainer` component for movie characters and favorites. How did it go? Would you still do that if you were to rewrite this project?

* 21 tests written (1 failing at time of assessment)
* In `App`, the `'should update state when submitUser is called'` test is a good start and looks good - a lot of other tests for methods missing
* Looking for an `updateFavs` test in `CharacterCard` to see that the function is called when the button is clicked and given the correct data
* If you're going to copy paste, remember to change titles for tests like `'should set state for radio button at index 1'`...
* Nice job testing the form with mock events! Would be nice to see a test for when the submit button is clicked and not all information is filled out in the form.

* No screenshots or gifs in README - get these added especially if you're putting this in your portfolio
* For Kanban board (GitHub projects), columns should be progression of tasks and not feature specific

## SwapiBox Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.

### Testing

* 2 - Nearly all unit tests are in place. Components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods (including `componentDidMount`).  No attempt to test async functionality was made.
