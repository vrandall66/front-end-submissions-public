### Evaluator: Robbie
### Students: Sara & Pol & Noah
### Comments:

* Really like the look of the movie cards - the text is very small, though
* What is the nav link animation supposed to convey? Not sure what it is
* With the search bar, even if it is selected, as soon as I mouse out of it, it collapses - not sure if the search bar is doing anything
* The redirect to the login if someone tries to favorite a movie while not logged in is good
* Just curious, why does the heart have a line through it?
* The individual show page for each movie needs some work, but I like the idea so far of the large image - the route for these will conventionally be `http://localhost:3000/movies/475557` (plural movies)
* Bug: originates on the Favorites page, the icon does not reflect that a movie is favorited, and when you click it, it copies the movie information to make the same favorite (this is why duplicate datasets can get you into trouble)
* Bug: clicking Sign Out from the favorites page does not sign out the user
* Good job having a placeholder on the Favorites page when there are no favorites

* Why use of `HashRouter` instead of `BrowserRouter`? (https://learnwithparam.com/blog/different-types-of-router-in-react-router/)
* Why the `fetchAndPostFavorite` and `fetchAndDeleteFavorite` action creators? Are you doing more of a middleware flow here?
* Good use of async await in your `App` file, how did you like that compared to more `.then()` chaining?
* Why the empty state in `App`?
* Routing looks very good in the `App` file, no redundant routes - there is probably an _overuse_ of `exact` in the routing
* Good error handling flow with the Login form
* In `NavigationBar`, is there a situation where you have a user in the store but they are not logged in? Just looking at what you are getting for props from the store: `isSignedIn: user.isSignedIn, name: user.name` - if not, this could cause state confusion if they are ever out of sync.
* For the `isLoading` reducer, the initial state is an empty string, but seems like it is being toggled between `true` and `false` - set the initial state to mimic the values that occur in the application

* 39 tests at time of eval
* Tests missing for `Form`, `App`, and `FavoritesContainer`
* Action and reducer tests look good - the `favorites` reducer tests are good because there are a few interesting paths for this reducer (compared to `isLoading`)


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
