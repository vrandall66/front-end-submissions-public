### Evaluator: Travis Rollins
### Students: Consuelo & Zoe & Sam
### Comments:

**Project Professionalism**
* Great work with your README including collaborators, setup, tech used, & screenshots.  Remember to include wireframes as well.
* Good amount of commits.
  * Remember to keep commits descriptive.  It can be hard to tell what actually was done if it is vague like [add passing tests](https://github.com/SamuelColeman/cinema-night/commit/411f79e7a717d4a77f6a7894390f693c8bb25a58) or [fix merge conflicts](https://github.com/SamuelColeman/cinema-night/commit/1a2ed458c23072d634c6af2facef476a8af89dbc).
* Good work being consistent with naming branches.  Could have more for the amount of commits ya'll had.
  * Most were descriptive but remember to be consistent so there aren't branches like `testing` or `clean-up`.
* Good work sticking with using your GH projects.  I appreciate Consuelo assigning herself to tickets.  Keep following this format.
* I really like this [PR](https://github.com/SamuelColeman/cinema-night/pull/22) where it is labeled as an `enhancement`, description on what the code is implementing, and the conversation/code review here.  Try and be consistent with this on most PRs.
* Several linter errors.  Remember to include the following in your `package.json`: `"lint": "eslint src/"` and then run `npm run lint`.

**Specification Adherence**
* Cool effect with animated background and transparent cards.
* With the menu, see how you can set it so the hover doesn't make it move.
* Good error handling with with the user needing to be signed in when trying to favorite a movie.
  * Wouldn't recommend having that error show up on every card.  It gets to be a bit much.  Maybe have a modal pop up or have the error display just once.
* On login, text on buttons are a bit too small.  I appreciate the coloring for hovers, but might keep the text the same size.
  * Good work with error handling for signing in with wrong email or password and if the email already exists when creating a new account.
  * Might disable the buttons if the user hasn't filled in the inputs.
* I might make it so that when the user signs up, they sign in as well.


**React Architecture**
* Should not need to update the DOM directly using things like `document.getElementById`.
  * Still with using conditional rendering and based on props, let React update the DOM
* Remember to use a `try/catch` inside of your form as well where you are doing async functions.  Without the `catch`, the app can crash at times.
* Interesting that there is updating of errors for local state and global state in the `verifySignIn` in the `Form`
  * How could you refactor to use similar pieces of logic for `verifySignIn` and `verifySignUp`.
* Good work keeping logic out of renders.
* How could some components be combined?  `FavouritesContainer` and `MoviesContainer` or `MovieCard` and `FavouriteCard`.
  * Keep practicing with refactoring so that you can reuse components.
* Good work with apiCalls.  Remember to check if the response is ok first before trying to do `response.json()`
* Some components have propTypes.  Be consistent so that all components have this.

**Redux Architecture**
* Good work of keeping track of loading and errMsg inside of the store.
  * Now remember to render a loading icon since you are keeping track of it.
* Good work keeping track of the user object
  * I would recommend not storing the password for security reasons
  * Also love the name....`pants`
* A bit of duplicate data because the entire object is being stored in the favorites array.  Potentially you could store just the unique movie_id and access the data from the movies array.
* Good work with your actions.
  * Should have an action for logging out as opposed to updating the props in your `signOutUser` method in `App`
* An extra reducer exists for the `password`.  Otherwise reducers look good.
* Similar to how you are using your actions for `isLoading` and `hasError`, in the `componentDidMount`, do the same  for `displayFavourites`
* For `bindActionCreators` like in the `Form`, you do not need the entire part about dispatching.  
  * You can set it up as `bindActionCreators({ login, signUp, hasError}, dispatch)`

**Testing**
* Good start with testing.
  * Some snapshots need to be updated and others have variables that have not been created making them break (like `action is not defined` or `signUp is not a function`)
* Alot of propType failures in the tests as well.  Double check that you are passing in props correctly.
* Good work in general on testing reducers.
  * Completely missing tests for actions.
* Quite a few apiCall tests are failing.  Read those warnings/errors
  * Some scenarios where the `received` does not match the `unexpected`.
    * For example, for `signUpVerification`, you have fetch resolving to the `mockCurrentMovie` instead of the `mockVerification`.
* For component tests, there are also some warnings with tests failing silently.
  * Things like `this.props.login` is not a function or cannot read property `preventDefault` of undefined.
* Some excellent tests for your `FormContainer` including changes in state and simulating events.
  * Good work even having a test using MemoryRouter!
  * Good work testing your `mapStatetoProps` and `mapDispatchToProps`.
* Some solid tests for your `componentDidMount` as well in your App.
  * Still plenty of methods that can be tested like `removeFavourite` and `toggleFavourites`.

**Routing**
* Good work in making all routes accessible in the UI.
* Hard to tell if the user has signed in.  Would be nice to have the user be taken to the movies page again along with displaying their name somewhere.
  * It also might be a bit of a confusing flow if the user signs out and they are automatically taken back to the login screen (as opposed to staying on the main page).
* A user likely shouldn't be able to view the favorites route if it doesn't exist.
* Look into how you can create a 404 page if the route doesn't exist.

## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.
* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  
* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.
* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods. There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps. No attempt to test async functionality was made.
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.