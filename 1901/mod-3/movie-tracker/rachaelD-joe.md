### Evaluator: David
### Students: Rachael, Joe
### Comments:
* Keep redundancies out of the store (they are technical debt)
* Be deliberate about error handling (use response info)
* Utilize helper functions to cleanup render or other methods SRP - each function should only have one responsibility

Your reducers tests are strange - the "should" statements are all related to app events - like clicks, etc. However, your reducers should be tested as isolated functions. The tests themselves seem good, but the "should"s make me unclear if you understand the tests as you're writing them.

Several of the component tests are skipped - particularly when it's stuff that is important to test (like functions/methods being called).

We are not testing mapStateToProps or mapDispatchToProps in our container components.

## Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal
  recommendations for design changes.


### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more
  than 5 linter errors. Project team makes large infrequent git commits.
  Project shows a basic understanding of React.

### Testing

* 1 - A valid attempt to test this application was made, but there are obvious gaps, with missing unit tests for Redux and React.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
