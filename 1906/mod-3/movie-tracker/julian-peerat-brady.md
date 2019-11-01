### Evaluator: Robbie
### Students: Julian & Peerat & Brady
### Comments:

* Just curious - why the window in the center of the page displaying everything? Why not use the whole screen?
* The redirect to the login if someone tries to favorite a movie while not logged in is good
* Good job with the show page for the individual movie, and good job with the routing convention (plural "movies" in the URL)
* No feedback on the Favorites page for no favorites yet
* How do I get back to the main page from Favorites?
* Nice job with keeping someone signed in after refresh with `localStorage`- however, there is an edge case where after creating account and being automatically signed in, refresh will sign out the user
* Bug: Why is there a "Sign In" button and a "Login" button on the same form? For Register page, there are two "Register" buttons

* Why isn't `App` in the Containers directory since it's connected to the Redux store? Similarly with other components - be sure to be consistent about this.
* Routing looks very good in the `App` file, no redundant routes - there is probably an _overuse_ of `exact` in the routing - some routes definitely need exact, but some do not and that could be confusing to other developers
* The initial page load flow getting the movies and checking for a loggedIn user is nice, especially with `localStorage`
* Talk about the need for a `temp` user, specifically around the `LoginForm` component
* What is the `Bounce` component doing for the `LoginForm`?
* In `LoginForm`, for the Login button logic, consider refactoring that so the `disabled` property is dynamically set (it can be `true` or `false`) to reduce the need for the two conditionals
* In `MovieCard`, the use of DOM traversing here `const curMovieId = Number(e.target.closest('section').id);` is not really necessary because you have the information you need in the function (`movie.id` from props) - when you see yourself doing DOM traversal like `.closest('section')`, ask yourself if you _really_ need to do this because as soon as the structure of the HTML is changes, DOM traversal can become very fragile and the code breaks easily

* Testing: 2 skipped, 41 passed
* Questions about the 2 that were skipped?
* A lot of proptype failures happening in the test suite

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
