### Evaluator: Travis Rollins
### Students: Emily & Greg & Katie
### Comments:
* Great number of commits.  Would recommend being even more specific at times.  
  * Ex: `Add action creator tests` may not be specific enough months down the line.  What if more actions get added later?  We'll need to write more tests.
* Good start to conversations on PRs.  Would like it even more to see reviews on comments on code.  What can be refactored?  What is still not working? etc.
* Good work keeping up with GH Projects
* Nice work on the README including contributors, description.  I might also include a part about setup for other developers as well as wireframes you used.
* Several linter errors, I would recommend adding in `"lint": "eslint src/"` into your `package.json` under `scripts` and run `npm run lint`.  
* Love how there are some albums already on display on `/` route
* Might run this app through an accessibility reader
  * Lots of red's and blues and for someone who is color blind, it could be challenging for them to make out details.
  * Interesting to note, the sound icon made me "as a user" want to click on it.  I expected it to play or do something.
* Love the creativity behind the hover effect to display more info on each Album.  Careful not to go overboard though.
* Good work displaying error if I try to favorite something without logging in. I might move the message to a different location.
* UI and scrolling get's a bit odd when I search for an artist but still see all of the previous ones.  I only get the 5 top albums.
  * Scrolling on mobile also gets a bit challenging.
* Might recommend using `type of password` for password input so others can't see user's password.
* Should a user be able to go to the `login` or `create account` page if they are already signed in?
  * Should clear out inputs when I create an account.
* Good work showing errors if account has already been used or if email and password don't match.
* Remember to move Component folders over into `Containers` if they are connected to the store
* Would look into how you can create a 404 page if the route doesn't exist.
* Good work with actions and reducers.  Very clean.  No duplicate data.
* Might recommend moving a few other things over to the Redux store like fetch errors and data for searchedArtist.
* All async functions in `componentDidMount` can be called in one try/catch.
* Good setup of using `.then` in `createTheUser`, `loginTheUser`, etc.
* Some unnecessary pieces of data being stored in state
  * Lots of properties in each of those objects that you don't need (hence the reason you have to clean it out when favoriting)
  * I might recommend cleaning the data before setting it to state.
* I might recommend mapping through all of the `WelcomeContainers` in the App component.
* Good work including propTypes.
* In `FavoritesContainer`, think about how you can refactor `isThisAFav` function.  Doesn't `includes` already return to you a boolean?
  * Likely don't need to do the `forEach` either here.  Map through your favorites, and pass a property of `isFav={true}` since you already know your favorites includes favorited albums.
* Might be some ways to refactor the two form components (especially reusing methods)
* Good work getting in most of the tests for `apiCalls`
  * Also solid tests for your reducers
  * Make sure all of your snapshot tests are up to date.  Also check that you are exporting/importing containers correctly.  You don't want to import the `connected` component like `Nav`.  Throw in an export in front of the function, and import nav with `{}`.
  * Same thing for `FavoritesContainer`.
  * Missing tests for mapStateToProps and mapDispatchToProps.
  * Would like to see some more tests in the future for `App` like that methods/actions have been called.  
  * Missing many component tests like changes in state and event simulations in Form components.


## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 
* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.

### Testing

* 1 - A valid attempt to test this application was made, but there are obvious
  gaps with missing unit tests for Redux and React.  
* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods.  All routes have been tested as well including dynamic routes.  There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps.  No attempt to test async functionality was made.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.