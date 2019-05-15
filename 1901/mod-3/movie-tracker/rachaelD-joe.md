### Evaluator: David
### Students: Rachael, Joe
### Comments:
* Keep redundancies out of the store (they are technical debt)
* Be deliberate about error handling (use response info)
* Utilize helper functions to cleanup render or other methods SRP - each function should only have one responsibility

## Rubric 

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal
  recommendations for design changes.
  

### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more
  than 5 linter errors. Project team makes large infrequent git commits.
  Project shows a basic understanding of React.

### Testing (PENDING)

* 4 - All requirements from 3 met, all async functionality is tested, tests are
  passing and run efficiently (using mount only when appropriate).
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all
  components are unit tested, and a valid attempt was made to test any async
  functionality.
* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test
  async functionality was made.
* 1 - A valid attempt to test this application was made, but there are obvious
  gaps, with missing unit tests for Redux and React.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
