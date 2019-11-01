### Evaluator: Travis Rollins
### Students: Chris & Matthew
### Comments:

**Project Professionalim**
* Excellent number of commits and keeping commits detailed
  * Good amount of branches.  Remember to be consistent with how you are naming branches.  Some are kabob case, others are snake case
* Great work with README having a table of contents with languages used, screenshots,features included, wireframes, etc.  Also great work including a link to your Project Board.
* Double check your linter (have a lot of linter errors including unused variables).  To check this out, include the script `"lint": "eslint src/"` in your package.json, and run `npm run lint`.
* Excellent work following a PR template describing what each one is including.
  * Remember to do some kind of code review and leave comments to show the continuous workflow before merging.
* In the future, make sure to ignore your apiKey file so it doesn't get pushed up to GH.

**Specification Adherence**
* Good work making it easy to access previous routes.
* Love the genres being included for each movie.
* A slight bug occurs when I try to `favorite` a movie without being logged in.  Movies disappear and I can't get them back.
  * No error message displaying when this happens (although I see it in the Redux store).
* Good work with modal.  Love the UI of the app.
* For creating an account, there should be some indicator to let the user know that the password must be a certain length.
  * Missing error handling if user tries to create an account that already exists.
  * Good error handling for logging in.  Likely shouldn't make the movies disappear though.
  * Good work looking into making sure that the email is formatted correctly.
* Favoriting a movie makes page refresh a bit.  See how you could fix this.
  * Good work with toggling though both on the main page and favorites page.
  * Great work including a notification if there are no favorites currently.

**React Architecture**
* I appreciate that you are starting to develop your own craft with React.
* Don't forget to include PropTypes!
* Remember to movie containers into the Containers directory.  (App, CurrentUser, LoginForm, etc.)
* Potentially could break out `mapping` like when deciding colors inside of `fetchGenres` into a separate function just to break things out more.
* How could we refactor `Favorites` and `Movies` containers into one? 
  * Good work reusing `MovieCard` component.
* For something like when `addFavorite`, it might look cleaner to pass the entire object through when invoking it.  
  * When initally fetching and setting the data in your array, set the properties how you want them to look.
* Gets a big div heavy in something like the favoriteCard component.
* Code can be a bit difficult to read through at times.  Try breaking properties out into multiple lines

**Redux Architecture**
* A bit of duplicate data with containing the entire movie object for favorites.
  * Essentially now we are containing data in the movies array and favorites.  Since each movie has a unique id, we could keep track of the id in the array, and then use that to match what is in the movies array.
* Otherwise, great work keeping the Redux store flat.
* Great work including loading and error properties.
* Good work with your actions and reducers and updating them as necessary.
* Excellent work with the Thunks and dispatching actions as necessary.
  * I would recommend keeping events inside of the component (instead of passing them to thunks).  It relates more to the DOM as opposed to the fetch.
* `ClickHandler` file should probably either live in a higher component or in a helpers directory, not thunks.

**Testing**
* Excellent work testing out actions, reducers, and Container functions.
* Missing quite a number of tests for something like the Form component.  (as well as the mapStateToProps & mapDispatchToProps).
  * Good work with snapshot tests but need to see more tests like changes in state in the Form and event simulations in the Card components.  Also make sure snapshot tests are up to date.
  * Good work testing mapStateToProps and mapDispatchToProps in App.  Try and include that in other Containers as well.
    * For something like mapStateToProps, try including extra properties in there so that you can tell that it is filtering out the properties you expect when it is run.
* Good work testing out your thunks and the different happy/sad paths for them.
  * Would like to see more async testing in the component/containers as well.  (Was this `postUser` method fired when they signed in.)
  * For a test like `calls dispatch with fetchRecentMovies when componentDidMount is called` inside of the `App.test.js`, we're not really checking if it was called after the component mounts.  After the shallow render of the component, check to see that those methods have been called.

**Routing**
* Notice you have duplicate routes for `movies/:id`
* Great work having routing available on all pages.
  * Look into how you can create a 404 page.

## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.
* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 
* 4 - The application completes all iterations above and implements one or more of the extensions.  The evaluator has no recommendations for design changes.


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