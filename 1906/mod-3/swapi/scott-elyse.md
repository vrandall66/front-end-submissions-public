### Evaluator: Travis Rollins
### Students: Scott & Elyse
### Comments:
* Good work with README including descriptions, setup, collaborators, and screenshots, and live project.
* Did you stick with your trello board?  I would also link that in your README along with your wireframes.
* Good work only having a couple of linting errors.  To check this, include this script, `"lint": "eslint src/" `, inside of your `package.json` and run `npm run script`.
* Great number of commits and being mostly consistent with detailed commits.
  * Some commit messages can be a bit more specific.  Like [tests for form](https://github.com/ec-myers/swapi-trivia/commit/7ea82fc59491b9058ee3216828c7c140ea3ad390).  What exactly did you test?
* I love it when I see conversations on [PRs](https://github.com/ec-myers/swapi-trivia/pull/13).  I would like to see more of this on every PR.  Test out the branch on your computer and leave a code review (even if you worked on it together).
  * Also it would be great to be consistent with a PR template including info like is this resolving a bug, adding a feature, or adding a test.  Etc.
* First start of the App, it breaks due to an error about PropType being not defined.  Double check bugs like this before evals (aka pushing something into production).
* Very clean interface.
  * LOVE the info that shows my profile information.  Very creative and nice subtle touch on the UI.
  * Excellent error handling.
  * Cool idea to show the scrolling text while its loading.
* Look into how you can create a 404 page if a route doesn't exist `/yolo`
* Good work with the toggling of favorites so it is clear to the user whether they are adding/removing a favorite.
  * I might store the info about how many favorites the user has next to the `Link` as opposed to being on each card.  (Could be confusing to the user on what the number means)
* Good work implementing localStorage as well (and good place to check if there is any data is in `componentDidMount`)
* A bit of a bug when trying to go to the `/favorites` route.
  * See if you can finish the `/favorites` route and I'll update the Specification Adherence score.
  * Interesting to note that on the `/favorites` route, you are passing cards and favorites as props (both with the value of favorites).
* Is there a way to keep properties like `haveFavorites` and `haveMovies` out?  
  * Can we check the length of the array?
* Good work breaking out fetches so it doesn't take forever.  Only fetch the data if the user goes to that route.  AWESOME!
* Cheers to using the error message and rendering it.  THANK YOU! 
* For displaying errors on the Form, how we could we refactor the conditionals?  For conditionals where the value is true or false, see if you can use the conditional logic.
  * Example `this.setState({ nameErr: !this.state.name })`
* Excellent work testing and including a wide variety of tests
  * Good event simulations, tests on methods and changes in tests, snapshots, and start to async tests.
    * Good work with tests for isolated fetches.  Remember to include a test for if the `Promise.resolves` but the property of `ok` is false.
    * Double check some of the warnings you are getting on tests as well.  (Errors like `Cannot read property 'slice' of undefined`)
  * I really love the test on line 59 in `App.test.js`.  Great work asserting changes in state and checking that the function was called.  Cheers!
* Good work with propTypes.  Take note that some of the proptypes are not passing in your tests.


## SwapiBox Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.
* 4 - The application completes all iterations above and implements one or more of the extensions.  The evaluator has no recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 
* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.

### Testing

* 4 - All async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).  Unit tests for snapshots and methods cover not only happy paths but also sad paths.  Evaluator has no recommendations for testing.