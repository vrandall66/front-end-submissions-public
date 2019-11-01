### Evaluator: Robbie
### Students: Kirk & Scott
### Comments:

* Seeing a failed proptype in the console on initial load
* Nice show page for each movie - the route for these will conventionally be `http://localhost:3000/movies/475557` (plural movies)
* Oooo, fancy login animation
* I like the halo around the favorited movies
* The form is a little confusing - why have the name field for when I am logging in and not creating the account?
* Nice screen for when there are no favorites - good idea to direct the user somewhere
* Good job with some email validation - the flash message is nice too

* Try to do something with those `console.error()` snippets in `App` - you can at least add some title to the error to make it clear where the error came from for debugging purposes
* In `App`, if this `Route path="/" render={ () => <Nav /> } />` is rendered for every route, which is why I am assuming you separated this route, then why use Router to handle that rendering? You can just put it in the App's render method at the top
* For App's `mapStateToProps`, why not use ES6 object initializing like you are elsewhere?
* For the `Nav`, good to see you utilizing NavLinks and their active state
* In the `Nav`, why not use `Link` instead of the anchor tags? `{user.name ? (<>{user.name} <a href="/login">Logout</a></>) : (<a href="/login">Login</a>)}`
* I'm curious in the `Login` component why is needs to keep track of `isLoggedIn` in its local state? Is this what is actually sending the user to the home page upon successful sign in and a re-render?
* In `Favorites`, a conditional like `if (!user.name) {` could be problematic. It seems like you're diving into the user's name because to see if there is a user, and empty object is truthy...but what if for some reason the name is empty or something else used to determine if the object is truthy is falsey? Consider making the initial user state `null` instead of an empty object. And then resetting to `null` upon signout to be absolutely clear there is no user in the app.
* Actions and reducers look great

* 73 tests!
* Questions about testing?

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

* 4 - All async functionality is tested. Asynchronous tests cover happy paths as well as multiple sad paths. All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing. (Try testing React Router.)

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
