### Evaluator: Robbie
### Students: Amy & Eduardo & Jon
### Comments:

* Use password input type (so it hides the characters from view)
* No feedback on the Favorites page for a user having no favorites yet
* Really like the movie show page with the image background
* Bug: if I create a new account the button for other user's favorites is still selected for the new user...

* For `App` class, interesting that you did not have a constructor in the class - do you know why this is still possible? For extending on the component without a constructor, how are you still able to use `this`, lifecycle methods, and render? Research this.
* Good use of async await in your `App` file, how did you like that compared to more `.then()` chaining?
* Routing looks very good in the `App` file, no redundant routes - there is probably an _overuse_ of `exact` in the routing
* In the form submit login, I might play around with the order of `setFavs(favs) updateFavs(favs) setUser(foundUser)`. It works as is, but there are interesting assumptions going on. I wouldn't think to be able to get the favorites before the user is set.
* This form validation logic is nice `disabled={!this.state.email || !this.state.password}` but might get long if more form fields are added - consider how you would handle a larger form.
* Tell me more about the need to nest buttons inside of the Header nav links - I wouldn't think this is strictly necessary.
* You have `FAVS` in both favorites and movies reducers - what is the distinction there? It might not be clear for other developers without really digging into it.
* Fetch calls in apiCalls look good
* Action creators look good

* 61 tests (1 failing, no tests for Header or MoviesContainer?)
* Would like to see input validation tests for the Login form and CreateAccount form
* A couple tests commented out in `CreateAccount` test - any questions there?

## Rubric 

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
