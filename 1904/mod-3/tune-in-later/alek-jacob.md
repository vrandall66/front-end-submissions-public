### Evaluator: Travis Rollins
### Students: Alek & Jacob
### Comments:
* Good number of commits
  * Overall most messages are detailed, remember to be consistent
  * Branches could be more specific in some scenarios (`delete`, `css`, `error-handle`)
* Good start with README with images and general info.  Could include a bit more documentation like `setup`, `goals of project`, `wireframes`, `project management tool`
* Good start with conversations on many PRs, but would like to see more than `looks great`.  Would be helpful to include code reviews and comments on specific lines on parts that could be refactored or bugs that are still existing.
* Several linter warnings that could get fixed.
* Great search functionality 
  * Appreciate adding functionality to search by genre if I don't have a specific author/book I'm looking for
  * Would recommend clearing out input if a user selects genre, or vice versa
  * Some bugs if user is on `favorites` route and a user clicks a genre or searches a book, nothing shows up.
* Lots of throwing errors that break app
  * Clicking show favorites breaks app if I'm not signed in
  * Favoriting an audio book also breaks app if I'm not signed in
* Should start out with `sign in` as opposed to `sign out` when I first open up app.
* Good start to dynamic routing, but not displaying info yet.
  * Super close with the functionality of this.  The data type of `book.book_id` and `match.params.id` are different.  Use `==` in your route in `App`. 
  * I appreciate the back button to be able to go back.
* Would look into how you can create a 404 page if route doesn't exist.
* When creating an account, it doesn't automatically sign me in.
  * No visual indication that it was successful.
  * I have to sign in after creating account.
* Good work showing error message if account already exists or incorrect email/password.
* Might be helpful to have a message on favorites page if no favorites exist yet.
* Would recommend moving components wrapped with `connect` into a `containers` directory
* In apiCalls, would recommend separating cleaner functions into a `helpers` directory.  Such as `fetchAudio`, you could create another function for the map for returning what data you need.
* Missing `try/catch` for initial fetch for `newSearch` as well as `fetchUserFavorites` and `postFavorite` 
* In `BookContainer`, if you need to pass all of the props, you can do so with with `<Book key={index} {...book} />`
* Login component likely could get refactored into smaller components
  * A component for signing in and creating account.
* Missing propTypes entirely.  Not going to doc points this time, but remember it for your final project.
* Would think about naming of reducers.  `getAudioBooksReducer` sounds like an action.  Would be okay with `audioBooksReducer` or even `audioBooks`.
* I appreciate having a couple of places for error messages.  I think it's okay for forms specifically to keep it in local state (nerd opinion though).
* Good work getting favorites only if user clicks on it.
* For `toggleFavoriteButtonReducer`, since it works as a toggle, think setting the value as a boolean would be fine.
* Redux store in general is pretty flat.  Good work!  
* Good start to testing, a lot of breaking tests though.
  * Double check the url for `fetchAudio`
  * Check snapshot tests.  For example, `Books`, make sure you are importing with just the component (not container).  Also remember to include props from store like `favoritesReducer`
  * Same for `Login.test.js` make sure to export just the component.  All tests are failing now because it's trying to import container connected to the store.
* Good simulation tests in `Login` component
  * Would continue those kind of tests in your `Book.test.js`
* Good work testing out actions and reducers.
  * Missing tests for some reducers, but ones that are there are solid.
* Good start with testing out apiCalls.  Well written, now test the rest of them!
* Good tests with mapStateToProps like in `Nav.test.js` and `App.test.js`
  * Keep working on tests for mapDispatchToProps

## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 

### React Architecture

* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  
* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.
* 4 - All requirements from 3 met, and no duplication of data exists in the
  store. Data in the store remains flat (not nested).

### Testing

* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods.  All routes have been tested as well including dynamic routes.  There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps.  No attempt to test async functionality was made.

### Routing

* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.
* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.