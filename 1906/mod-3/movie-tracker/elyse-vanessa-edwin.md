### Evaluator: Travis Rollins
### Students: Elyse & Vanessa & Edwin
### Comments:

**Project Professionalism**
* Excellent number of commits.  Good work in general with consistency on commits.
  * A few could be more descriptive like [Fix bugs and improvements](https://github.com/ec-myers/the-screening-room/commit/363c14fe8e478e2d20e460ee1899587e8b6d1909) or [fix broken tests from merge](https://github.com/ec-myers/the-screening-room/commit/371f43e7be28f079d3a8c84150b3d61030831044).
* Great work adding tags for PRs including whether it is a bug, enchancement, etc.
  * I appreciate the templates and what ticket it is resolving and having some code reviews.  Great work and continue to do this more consistently.  Example is [here](https://github.com/ec-myers/the-screening-room/pull/34).
* Decent amount of branches but could have more.  I appreciate the consistency around using initials for who creates what branch and what functionality it handles.
* Great work with your README including the summary, developers, screenshots, setup, and technology used. Remember to also include wireframes and kanban board used.
  * I appreciate the couple of GH issues that were included for the future.
* Also, cheers to having no linting errors!
* Potentially for the future, look into a rebase workflow.

**Specification Adherence**
* Nice styling of the main page.  Like that the header always has a different background image.
* Great work with the login modal and ability to toggle between Logging in and creating an account.
  * Great error handling on the forms.
  * Maybe have the button disabled until all inputs are filled?
* Great work with the extra details as well for each movie.  UI is very clean and intuitive.
* Noticed you were keeping track of `isLoading` but not showing a loading icon.
* Potentially might not include the `Favorites` route if the user hasn't signed in yet.
  * Might include a note of the user doesn't have any favorites yet.
* I really like the counter on the `Favorites`.
* Great work implementing localStorage.
  * I appreciate when I logout, it clears the localStorage as well.

**React Architecture**
* Good work creating a containers directory.
  * Now remember to move your directories over that are hooked to the store like the `App`, `LoginForm`, etc.
* Good work checking propTypes including props from the store.
* Good work with your apiCalls.
  * Would recommend moving the cleaning functionality in your `getMovies` function into a cleaning file.  Same with the wallpapers.
  * I appreciate the consistency in checking if the response is always ok.
* In the future, I would recommend keeping the apiKey in a separate file and ignoring it so it doesn't get pushed up to GH.
* Good work destructuring props and calling actions when necessary like in `componentDidMount`.
* Does the `markedMovies` variable in `loadMovieData` need await?  Is there any fetching going on in there?
* I'd see how you can refactor the `loadMovieData` and `updateFavorite` even if it's breaking it out into their own functions.
  * It might help with readability & testing too since having conditionals and then a nested try/catch can add more complexity.


**Redux Architecture**
* Good working including `errorMsg` and `isLoading` properties in the store.
* A bit of duplicate data being stored because of the entire object being stored in the `favorites` array.  
  * Potentially you could store just the movie_id and use that to find which one it is in the movies.
  * emailErrMsg probably could be stored in the `Form` component.
* Excellent work with your actions and reducers.
  * A few extra parenthesis that don't need to be there like `return (state = []);` in the `favorites` reducer.

**Testing**
* Excellent number of tests!!
  * Great work testing your actions
  * For reducers, I appreciate testing that if the type is not correct, the initial state should be returned.
    * You should still have a test if the case is correct though for happy path testing.
    * Remember to include this for future projects as most of the tests for reducers are for the default state.
    * Great work with your `movies` reducer tests.
* Double check the handful of warnings for your apiCall tests.  ApiCall tests are odd in that they sort of `pass` but silenty fail with the warnings/errors.
  * Something like where it says `cannot read property map of undefined` means that something isn't quite mocked right.  It isn't able to finish the function and map through it.
    * For example in your `getMovies` test, you have it resolving to an array of objects.  However if you look at your implementation, it running `json()` actually results into an object with a property of `results`.  This results property has the array of data to iterate through.
  * There is another warning that mentions it received `undefined` instead of the array.
* Good work testing your app with mapStateToProps and mapDispatchToProps
  * Would like to see more unit testing for React aside from the snapshot test.
    * Try testing your `componentDidMount` to make sure methods were called.  Also try testing that methods were called in `updateFavorites` or `loadMovieData`.
    * Something like testing `markFavorites` could be useful to see if it returns what you expect. 
* Good work testing out your Form component with changes in state and doing event simulations.
  * Shouldn't need the `forceUpdate` on some of the tests because you have a callback functions.  
    * In order to make those tests pass like `'should invoke handleChange on change of email input when error is true'`, make sure you assign the mock function to the method like `wrapper1.instance().handleChange = jest.fn();` 

**Routing**
* Some great work with the refactoring of routes 
  * Example is `<Route path='/(|movies|signup|login)'>`
* Great work making all routes available on all pages.
* Look into how you can create a 404 page if the route doesn't exist.
* In the Nav component, how could you refactor the `NavLinks` for the logging in/signing up?
  * The are relatively similar to each other aside from the `to` prop and `onClick`.

## Rubric 

### Specification Adherence

* 4 - The application completes all iterations above and implements one or more of the extensions.  The evaluator has no recommendations for design changes.

### Project Professionalism

* 4 - Codebase has zero linter errors/warnings and README is well documented with images of different pages, setup, purpose of application, and group members. Project team uses a rebase workflow, taking advantage of github issues to track work.

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.
* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.
* 4 - All requirements from 3 met, and no duplication of data exists in the store. Data in the store remains flat (not nested).

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 4 - All async functionality is tested. Asynchronous tests cover happy paths as well as multiple sad paths. All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing. (Try testing React Router.)

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.