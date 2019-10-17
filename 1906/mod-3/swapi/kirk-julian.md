### Evaluator: Robbie
### Students: Kirk and Julian
### Comments:

## SwapiBox Rubric

* For spec adherence, everything looks good!
* The movie colors are nice and bright - not my style, but I like it overall - that look and feel didn't quite carry over into the characters list, but it was still easy to use anyway
* The loading animation is great!

* Nice job breaking out functions for the apiCalls
* In the `getFilmCharacters` function, `.then(data => data.characters).then(data=> data.splice(0,10))` looks like it can be done within the same `.then()` just as a multiline instead of passing through another `.then()`
* `<Route exact path='/movies'` is listed twice, but one has `exact`, tell me more about this decision (usually you want to have one route `/movies`, and within that decide what to render)
* Nice job using the `key={movie.episode_id}` episode id instead of the `map` index in `MovieContainer`

* 38 tests passing - a proptype failure occuring at time of assessment
* The `Form` tests look great! Any questions about these?
* For the `Should call setFavorite when the button is clicked` test, it would also be great to see that the method was called with the correct arguments

* I like the DOCS directory in your project - nice to have everything in one place instead of random gists
* Overall, nice job with your kanban board

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