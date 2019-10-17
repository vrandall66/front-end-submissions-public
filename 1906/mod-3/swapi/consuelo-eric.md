### Evaluator: Travis Rollins
### Students: Consuelo & Eric
### Comments:
* Good work with the README
  * Appreciate pics, and overview.  I might include a description describing purpose of app as well.  Remember to include wireframes in your README as well.
* Good work continuing to use GH Projects and issues.
  * Would like to see cards broken out even smaller instead of by iteration (by bug, feature, test, etc.)
* Great number of commits and commit messages.
  * Some commits could be a bit more specific.  What did the [merge conflict](https://github.com/ericwm76/planet-crait/commit/91af1e3377301e724b6706f9cc0e96dc542d9a36) resolve?  What [api calls](https://github.com/ericwm76/planet-crait/commit/2ea202d79e8f952377ab0ba57df27065b630483e) were tested? What [snapshot tests](https://github.com/ericwm76/planet-crait/commit/c63b739a169cba7c92844e37782d3f1d8c96399a) were written?
  * Would like to see more branches and PRs as well.
  * I appreciate a couple of messages on some of the PRs, but would like to see it for every PR.  Pull the branch down, test it out, and leave a code review for each PR (yes, even if you worked on it together)
* Fun video on the Form, captures the spirit.
  * Might give a bit more spacing around inputs.  Some of the glow on hovers get into inputs.  
    * In general styling could use a bit more polished like the text for "no favorites".
  * Would have some kind of active state on buttons to know if I clicked on `Novice`, `Expert`, etc.
* Good work sorting of movies and including images.  Nice touch.
* Careful about adding hovers for the card as well.  
  * Can make the user think they can click on it when really the user must click on the `View Characters` button.
* Great route handling making it easily accessible in all scenarios.
  * Might remove the `Movies` button route when the user is already on `/movies`.  
* Some broken functionality with favorites.
  * Able to add duplicates.  Unable to turn them off it seems. Hard to tell which characters are actually favorited (no visual cue).
  * Also challenging to find where the user should click to favorite a card.
  * Think about how you are storing each favorite.  Currently you are storing the entire object into another array inside of state.  This creatures duplicate data inside of our state.  Maybe another way could be to add a property of `favorited` to each character object?  Default it to false, and then update as necessary when a user clicks on a character card.
* Look into how you can create a 404 page if I go to a route like `/yolo`
* 6 linter errors.  Add in the script `"lint": "eslint src/"` into your package.json and run `npm run lint` so you can see your linter errors.
* Make sure to do something with errors for fetches.  Set them in state and render them!
* For the setting of a user to state, I think it's find to have a user object instead of 3 properties inside of state.
* In `selectMovie` in App, do we need to set all of the data to state?  Or do we just need the characters?
  * Might recommend cleaning out the data
* Double check in your `updateFavorites` to make sure you aren't adding duplicates.  Maybe a conditional to check if it `includes` it?
* In renders, I would recommend breaking out props onto separate lines for readability reasons.
* How can we refactor MoviesContainer, FavoritesContainer, and CharactersContainer?
* Love some of the fetch functions like `getFilms`, `getHomeworld`, etc.
  * Remember you don't need a `catch` inside of the apiCalls.  Keep the `catch` in the component so you can set it to state.
* Good start with the test written for `getMovieData`.
* Good variety of tests including snapshots, methods/changes in states, event simulations, and async tests. (especially like your LandingPage and App component)
  * A few failing snapshot tests.  (some need to be updated, another is suddenly getting `undefined`)
  * Good work mocking out some async functions and checking that they were called.  Now check if the state has been updated!
* Cheers to including propTypes!


## SwapiBox Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.
* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 
* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.

### Testing

* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.
* 4 - All async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).  Unit tests for snapshots and methods cover not only happy paths but also sad paths.  Evaluator has no recommendations for testing.
