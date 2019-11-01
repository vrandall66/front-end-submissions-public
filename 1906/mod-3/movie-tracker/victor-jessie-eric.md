### Evaluator: Travis Rollins
### Students: Victor & Jessie & Eric
### Comments:

**Project Professionalism**
* Decent amount of commits and branches.
  * Many good detailed commits.  Some could be a bit more descript like [write normal and async tests](https://github.com/VPAbraham/movie-tracker/commit/bdac130544d562fd510b5c6e49ea4dc7bc2a5c9c).
  * Good work being consistent with naming of branches.  Again, a few could be more specific like `async-testing-2` and `component-testing`.
* Great work with the README including tech used, demos, and credits.  I would recommend including links to each name to their GH profile.  I would also like to see a link to your kanban board used and wireframes and setup instructions.
* Several linter errors.  Make sure to add in a script in your package.json like `"lint": "eslint src/"` and then run `npm run lint`.
* Good work on some PRs having some conversation.  Think the PR could still have a more formatted template and maybe using GH labels to describe if it is an enhancement, bug, test, etc.  Still would like to see some code reviews and consistency with conversations on PRs.

**Specification Adherence**
* Really cool hover effect for the Movie Tracker logo/link
* Nice work displaying movies.
  * A bit confusing having to scroll up and down instead of left and right.  I might have movies listed vertically as it is more natural especially on mobile to scroll up and down as opposed to horizontally.
* I like the info icons.  The text is very small and challenging to read though.  I might have just either the icon (hoverable) or make the text bigger for more information.
* Cool setTimeout if a user tries to favorited a movie without being logged in.  
  * Displays and then disappears.  Nice touch.  Again, the text is a bit small so I might make it a little bigger.
* App breaks if I try to create an account that already exists.  Look into doing some error handling.
  * Good error handling though if I try to sign in and the email or password doesn't match.
  * I might set it so it that the button is disabled until the user has filled out all inputs on the form.
* Text for forms can be a bit challenging to read.  Might run the app through an accessbility reader.
* Could be interesting to do more user testing to see how people react with the arrows on the favorites/movie routes.  Are they trying to click on them or does the user know that it's meant to signify that it's the beginning/end?
  * Toggling of favoriting still works as expected though.

**React Architecture**
* Good work keeping logic out of render
* Make sure to do something with an error when it hits a catch.
  * Example is in `submitNewUserInfo` in the `Form`.  Currently it throws an error and breaks the app.
  * Same idea in the `componentDidMount` inside of `App` where the error is being console.errored.
* Good work including propTypes.
* Wondering how the `LoginForm` and `NewUserForm` could be refactored into one.
  * Might need some conditional logic but could be fun to try and refactor.
* Great work reusing the `Card` component.  
  * How could the `FavoritesContainer` and `MoviesContainer` also be refactored?
* Might look into how `toggleFavorites` can be refactored.
  * Some nested conditionals happening here and can be both hard to read as well as add extra features to it down the line.  Also should not need to be running `forceUpdate`.  If the action updates the store, it should re-render.  Or maybe use a lifecycle method like `componentDidUpdate`.

**Redux Architecture**
* Good work keeping the Redux store flat and not nested.
* A little bit of duplicate exists in the global store.
  * Instead of storing the entire object of the favorites array, look into how you could store just the `movie_id` and reference that to the movies array in the store.
* I might add in a couple of properties in the store like errorMsg if a network request fails for getting the movies or an isLoading for a user who has a slow network.
* Actions look solid as do the reducers.
  * Maybe a scenario where the `login/logout` could be refactored into one based on the argument you pass.
* Good work moving components connected to the store into the `containers` directory.
  * Still several that could get moved over like the `Form`, `Nav`, `Movie`, etc.

**Testing**
* Good start with number of tests.
* Some tests failing either because snapshot is returning undefined.  Others need to be updated.
* Other tests failing like `mapStateToProps` is not a function.
  * Example is in `NewUserForm`.  There is no `mapStateToProps` being used.
* Good start with tests for actions.  If you had more time, I would try and test them all.
* Great work testing your reducers.
  * A couple scenarios where it fails because the way it is being mocked out doesn't match what the implementation is looking for. (for example the favorites reducer).
  * For some tests, what you expecting it to be doesn't match up.  It actually is working the way it should.  For example, in the `isLoggedIn` reducer, `should be able to log out a user`, the returned value is false.  That is what you want the new state to look like.
* Good work trying to test out your isolated fetch calls.
  * Double check and read some of the errors/warnings that the test suite is giving you.
  * Some of them are so close but the error you expect it to be is off by a period.
  * Others a different error is being thrown instead depending on how you mocked out the fetch.
  * Some are running into a situation where it is hitting a `response.json` but json isn't a function.  Many are just typos, so go back through and double check them.
* Some good tests in the `LoginForm` component to check that state has been updated.
  * A bit confused why there is a test for `mapStateToProps`.  There should be a test for `mapDispatchToProps`.
  * Same for your `App`, write out some tests for `mapDispatchToProps`.
* Try testing out some of the async methods in here as well like `loginUser`.
* Good work testing your `componentDidMount` in the App.
  * Follow that same path and test your methods like `AddFavorite` and `removeFavorite`.
* Could have a test for the `Card` component where you simulate an event for clicking the button and making sure it calls `clickFavIcon`.

**Routing**
* Good work making all routes accessible on all pages.
* Would look into how you can create a 404 page if a route doesn't exist.
* Some scenarios where defining a route should be using the `component` prop as opposed to `render` since there is no data being passed. (examples are `LoginForm` and `NewUserForm`).

## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.
* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 
* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.
* 4 - All requirements from 3 met, and no duplication of data exists in the store. Data in the store remains flat (not nested).

### Testing

* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods. There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps. No attempt to test async functionality was made.
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.