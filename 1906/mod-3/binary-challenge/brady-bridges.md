### Evaluator: Travis Rollins
### Students: Brady Bridges
### Comments:

**Project Professionalism**
* Good number of commits but make sure to keep them descriptive.
  * A lot of testing commits but don't describe what you are testing.  Or an `add routes` commit, but what routes are you adding?
  * Good work with branch names.
* Good work starting out with the GH Project, but make sure to continue to update it.
* Great work using a table of contents with your README including objective, setup, and different screenshots.
  * Would recommend including wireframes as well.
* Good work with having pretty much no linter errors!

**Specification Adherence**
* Excellent work creating a mobile first app.
* Really love the different tabs to view the different coins.
  * Pretty cool to check out values and untrack ones I'm not as interested anymore.  Very creative.
* Great work including localStorage as well.
* Might include an active state on the `NavLinks` so the user knows which one they are on.

**React Architecture**
* Good work breaking out the apiKey into its own file.  Remember to `gitignore` it next time so it doesn't go up to GH.
* Good work keeping components and containers in their respective directories.
* For `PortfolioInfo`, I think this could be a functional component instead of class since there is no need to keep track of state.
  * No need for the method, can just map through.
* Good work including propTypes
  * Remember to include propTypes for props from the store.
* Great work breaking out your apiCalls and checking if the response is ok before doing `response.json()`.
* Don't need to include an `.eslintrc` file.  React already has its own linter.
* Interesting idea for the `handleCryptoRefresh` function in App.
* Good work handling errors in your catch.
  * Remember to render the error.
* A lot of places where you have to do `Number(data).toFixed()`
  * Would recommend doing this earlier when you set the data so you don't have to do this again and again in every component.


**Redux Architecture**
* Good work keeping store pretty flat and not nested.
* Nice work including an `errorMsg` property.  I would also recommend including an `isLoading` property as well.
* Great work with your actions and reducers.
* In general good work using mapStateToProps and mapDispatchToProps where necessary.

**Routing**
* Routes are extremely clear and easy to view different pages.
* Potentially see how you could include a 404 page if a route doesn't exist.
* Great work with the dynamic routing and using the `match` object for the `CoinInfo` in `App.

**Testing**
* Excellent number of tests and NO WARNINGS!  THIS IS AWESOME!
* Good work testing actions and different scenarios of reducers.
* Really nice work testing all scenarios for apiCalls.
* Good work testing `mapStateToProps` and `mapDispatchToProps` in your App. 
  * Good attempt at testing your `getCryptos` method.  Try and test out some of the other methods in there as well.
* Good work testing changes in state in your `SearchCoins`. `handleCoinSearch` is also on the right track.
* Good efforts towards testing simulating events as well.  The simulation in `TimeFrameBar` was excellent.

## Rubric 

### Specification Adherence

* 4 - The application completes all iterations above and implements one or more of the extensions.  The evaluator has no recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 4 - All requirements from 3 met, and no duplication of data exists in the
  store. Data in the store remains flat (not nested).

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 4 - All async functionality is tested.   Asynchronous tests cover happy paths as well as multiple sad paths.  All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.