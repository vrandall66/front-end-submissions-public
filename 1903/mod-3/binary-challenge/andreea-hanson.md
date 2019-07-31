### Evaluator: Travis Rollins
### Students: Andreea Hanson
### Comments:
* Great number of commits
  * Good consistency with breaking out commits and commit messages
  * Good work making PRs and creating branches
  * Nice work setting up a GH project to track your progress!
* Excellent work on your README
* Would work on making your app mobile friendly.
* Nice work with route handling
  * Cheers to having a 404 page.
* Yay for propTypes!
* Nice work showing a loading screen when waiting for the data!
* Nice work with the favoriting functionality
  * Good work only storing the ids that you need for the favorites.
  * Good work keeping store flat.
* There are several props that are unneeded in the `DetailsPage` that are needed.
  * Don't need match, toggleFavorite, id, etc.
  * Same for mapStateToProps, don't need mascara, lipstick, etc. in mapStateToProps
  * Only bring in data that is needed in that component
* Test for mapStateToProps for `DetailsPage` is a bit off.
  * Add in some extra props that you don't need, and then test to make sure that mapStateToProps returns what you expect to get back.
* Would recommend refactoring NavBar as well.  Each method could get reused
  * Good logic for checking if something is in store so it doesn't re-fetch
* Would separate reducers into different files for each makeup type as well as favorites
* Good work with tests for actions & reducers
* Likely can clean up routes in the App
  * Either loop through, or make the first part of the route dynamic
    * `/:type/:id`
* Sometimes not using beforeEach 100%.  Noticing initialState being rewritten multiple times in App test
* Nice work with apiCalls and testing it

## Rubric

### Specification Adherence

* 3 - The application uses the above technologies to a professional level. The evaluator has minimal recommendations for refactoring or design changes.
* 2 - The application is in a usable state, but is missing part of one or more of the technologies outlined above. Evaluator has multiple recommendations for design changes.

  [10 Essential Usability Guidelines.](https://speckyboy.com/10-essential-web-application-usability-guidelines/)

### Project Professionalism

* 4 - All requirements from 3 met, codebase has zero linter errors/warnings and readme contains screenshots of application. Project team uses a rebase workflow, taking advantage of github issues to track work. Project shows a complete mastery of React architecture.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 4 - All requirements from 3 met, and always chooses the correct component for rendering, as well as the correct Route API. Application should account for undefined routes.
