### Evaluator: Leta
### Students: De'Marcus Kirby
### Comments:

* Consistent descriptive commit messages
* No use of PRs
* README is fine
* Redux store has redundant data (favorite) - should only include id, current episode, and comment
* Only console logging errors, rather than setting them in the store to be used
* 404 page handling
* Console logs still hanging out in code - remove
* Nice dynamic routing
* No proptypes
* MISSING mapStateToProps and mapDispatchToProps tests!
* MISSING component method tests

PROJECT FAILING!
Extension due Thursday @ 9pm:
  - Complete and pass testing (see notes above)
  - Implement PropTypes  

## Rubric

### Specification Adherence

* 3 - The application uses the above technologies to a professional level. The evaluator has minimal recommendations for refactoring or design changes.

### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more than 5 linter errors. Project team makes large infrequent git commits. Project shows a basic understanding of React.

### Testing

* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test async functionality was made.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 4 - All requirements from 3 met, and always chooses the correct component for rendering, as well as the correct Route API. Application should account for undefined routes.
