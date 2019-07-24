### Evaluator: Travis Rollins
### Students: Kayla Larson & Nathan Froehlich & Emily Dittmer
### Comments:
* Great work being able to click outside of the login page to close out
* A couple bugs with not being able to favorite on the favorite page.
* Keep working on functionality for logging in after creating an account.
* Spend a little more time on CSS with the header and making sure movies don't overlap on each other.
* Look into creating a 404 page for an non-existant route.
* If you need child components to have access to history, location, & match, utilize withRouter.
* Would recommend using the Link component from React Router instead of the history prop for going to a different page.
* Make sure everything include dispatches and state from Redux store are tested in propTypes.
* Little extra data in the store that doesn't need to be there.  Store the movie_id instead of the entire object in the favorites array.
* Good work on testing components, actions, reducers.  Would add more tests for containers including mapStateToProps & mapDispatchToProps.  
* Continue to work on consistency with leaving comments for PRs.  Good amount of commit messages and README.

## Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the  features outlined above. Evaluator has multiple recommendations for design changes.

  [10 Essential Usability Guidelines.](https://speckyboy.com/10-essential-web-application-usability-guidelines/)

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test async functionality was made.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
