### Evaluator: Travis Rollins
### Students: Quinne & Lacy & Jeannie
### Comments:

**Project Professionalism**
* Great work with your README.  I really appreciate the wireframes and data flow chart along with the screenshots of your application. Also cheers to including contributors and setup.
* Excellent number of commits.  May be the most I've seen on a project!
  * Good work with consistency with commit messages
  * Good work with consistency with branch names.  Some could be a bit more specific like `testing-one, testing-two, etc.` or `styling-three`.
* Several linter errors so remember to include the script `"lint": "eslint src/"` inside of your package.json and then run `npm run lint`.
* Good work keeping track of current issues and continuing to work through using your kanban board.  
  * I appreciate highlighting who is working on which tasks, when a task matches up with an issue, and which iterations each task is resolving.  This was excellent!
* Good work leaving thoughtful responses to PRs and following a template.  Potentially could add GH tags for each PR as well (to highlight whether something is an enhancement, bug, test, etc.)

**Specification Adherence**
* Good styling of the extra details pages and the forms.  I think the home page could utilize more space.
* Scrolling up and down to make it go left and right creates a confusing UX. 
  * Would have them scroll up and down.  Is more natural for mobile users.
* Not a huge fan of alerts popping up when a user clicks on favoriting a movie.
  * Maybe have a modal pop up or a message that appears on the DOM.
* Good error handling if user already exists when creating a new account.
* I appreciate options on both signing in and signing up to give the user the option to go to the opposite page.
  * Would be nice to have an option to go back to the movies page though.
* After checking out more details on a page, would like the option to go back and view all movies. **Fixed**
  * Same when i'm on the `/favorites` route. **Fixed**
* Would like to see some kind of message if there are no favorites currently.
* Good work with toggling functionality working on both favorites and root routes.

**React Architecture**
* Good work making sure your containers are in the containers directory.
  * Remember to move your `App` over there as well since it is connected to the store.
* Look into how you can refactor the `toggleFavorite` method.  Nested conditionals get a bit complex. 
* Careful of having functions inside of functional components like the `handleClick` in the `Movie` component.  Unable to test it as a result of this.
* In the `Movie` component, there are some scenarios where you are using shorthand in objects and othertimes not.  Be consistent    * Example: `() => selectMovie({ movie_id, title: title, poster_path, release_date, vote_average, overview})`
* Good work creating a helpers file for your cleaning functionality.
* In your apiCalls, remember to be consistent with checking if property ok is true or not.
* Good start with propTypes.  Make sure you are checking all props including ones coming from the store.

**Redux Architecture**
* A little bit of duplicate data in the store.
  * Storing the entire object in `favorited` as well as `selectedMovie`.
  * That data already exists in the `movies` array.  Potentially we could store just the unique movie id in both favorites and selectedMovie, and then find which one that connects with to the movies.
* Overall, store is pretty flat.
* Good work with most actions.
  * Some extra data being passed through that likely doesn't need to be passed in actions.  For example, `logoutUser` likely doesn't need the current user because you are setting the reducer to `null`.
    * Same idea for favoriting, could likely toggle the favorited by doing the opposite of what state is.
* Overall great work on your reducers.
* In form component, quite a bit conditional logic happening here.  Instead, the places where you are checking to see if the response is ok or the status of the response, keep that in the apiCalls.  Then any errors that get thrown, use a `catch` inside of the methods in the Form.  Always have a `try/catch` when using `async/await`.

**Testing**
* Excellent number of tests.
* Double check, there are a few propTypes warnings due to what what is being passed when you shallow render components.
* Great working testing your actions
* Good start with testing reducers.
  * A few scenarios where something like `deleteFavorite` is not working because your mock movie data has `id` instead of `movie_id` properties. **Fixed**
* Great work with testing your apiCalls.
  * Remember to have 2 sad path tests.  One for if the promise resolves but the property of ok is set to false (like you had), and another if the Promise rejects.
* Great work testing your Form component including methods and changes in local state as well as mapStateToProps and mapDispatchToProps.
  * Make sure you have another test for mapDispatchToProps for `retrieveFavorited`.  Same thing in the App for all of the methods you have in there.
* Some components could have more React unit testing.
  * In something like the MovieCard, have some simulation events to make sure functions are called.
* I would have a separate describe block from each other in `App.test.js` as opposed to nested describe blocks.  Gets challenging to read and follow.
* In `App.test.js`, for the test `'should return array of favorited movies for currentUser'`, I think the idea would be to check that `fetchData` has been called and also check what it returns when invoking `getFavorites` as opposed to checking what `fetchData` returns.
  * Try and include some tests for `componentDidMount` and `toggleFavorite` as well.

**Routing**
* Looking into how you can create a 404 page for a route that doesn't exist.
* Some routing issues with the user not being able to go back to the home page on the forms, favorites, and extra details routes. **Fixed**
  * Maybe the Title route to take the user back to the home page could have a hover effect to make it easier for the user to see that it is clickable.


## Rubric 

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 
* 4 - Codebase has zero linter errors/warnings and README is well documented with images of different pages, setup, purpose of application, and group members. Project team uses a rebase workflow, taking advantage of github issues to track work.

### React Architecture

* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  
* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.
* 4 - All requirements from 3 met, and no duplication of data exists in the store. Data in the store remains flat (not nested).

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.
