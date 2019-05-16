### Evaluator: Will
### Students: Lauren, Sally
### Comments:

Make sure your reducers are named to match the property of the store they are updating/using. Instead of "setFavoritesReducer", it should be "favoritesReducer".

Linting is poor - indentation is all over the place.

Architecture is shaky - make sure containers are in the containers folder.

Testing is very thin. Many tests are missing or inappropriately using assertions. Functionality of redux is mostly tested (actions, reducers), but very few component tests are thorough, including both snapshots and proper testing of functions. Asynchronous testing is absent.

## Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal
  recommendations for design changes.

### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more
  than 5 linter errors. Project team makes large infrequent git commits.
  Project shows a basic understanding of React.

### Testing

* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test async functionality was made.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 4 - All requirements from 3 met, and always chooses the correct component for
  rendering, as well as the correct Route API. Application should account for
  undefined routes.
