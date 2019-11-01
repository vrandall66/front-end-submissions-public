### Evaluator: Robbie
### Students: Michael & Ayla & Kate
### Comments:

* Like the Netflix theme to it - the box shadow is _heavy_ - remember a shadow is supposed to mimic light and a real object with dimensionality
* The login hover state is nice
* Use password input type (so it hides the characters from view)
* Pressing "Enter" on the login form brings me to the Create Account form - play around with how to change that
*** No favorites page**
* The favoriting star is nice - pretty obvious and clear that it has been favorited

* For `App` class, interesting that you did not have a constructor in the class - do you know why this is still possible? For extending on the component without a constructor, how are you still able to use `this`, lifecycle methods, and render? Research this.
* Routing looks very good in the `App` file, no redundant routes - there is probably an _overuse_ of `exact` in the routing
* The naming of this action creator/function is very confusing in `App` - `this.props.isLoading(true);` - I would expect `isLoading()` to be something that checks the status, but not a function to _set_ the status (`setMovies()` is clearer)
* For `retrieveFavorites` in `App`, I'm wondering about the need for `if (id) { ...` without an else case - what is the case where this would not be passed an `id`, and can this be caught earlier to be sure that `retrieveFavorites` is only called when there is an `id`?
* Tell me about the `buttonClick: false` property on the `Login` component state - what is it's use?
* Logging in the user is happening in the `App` with `loginUser` and not on submission of the form? This flow is a little confusing to me. I would expect the login POST request to happen on the login form submit, and if it's successful then it would take you to the main page again.
* Tell me more about the faves array and the movies array - how do those two interact?

* 20 tests passing at time of eval
* Many components are missing any tests beyond snapshots
* No reducer or action tests that I can see

**Need to create action and reducer tests** - Have these deliverable by 12pm Thursday - completed on time.

## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods. There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps. No attempt to test async functionality was made.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
