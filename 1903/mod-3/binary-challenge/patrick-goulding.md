### Evaluator: Leta
### Students: Patrick
### Comments:

* UI is really bad for accessibility and doesn't demonstrate usability or mastery of Front End development concepts
* Why are ingredients crossed out in drink info cards?
* When finding drinks by ingredient, should be able to click drinks to see more details instead of having to search for them
* No 404 handling
* Favorites not showing up
* No cocktails stored in Redux store except for favorited ones
* Actions and reducers are not tested at all
* Should be destructuring `drinkCard` in DrinkCard.js
* Missing several component tests
* Missing entire test suites
* Commit messages are inconsistent
* Low number of commits
* Low number of PRs
* No PropTypes
* Linter is showing no errors

PROJECT IS FAILING
Extension due Thursday @ 9pm:
  - Get favorites rendering
  - Write tests (ALL actions, ALL reducers, at least one container's component methods, ALL component snapshots, at least one container's  methods, at least one container's mSTP and mDTP, async tests), get them passing

## Rubric

### Specification Adherence

* 1 - The application is missing multiple features outlined above. Developer did minimal to no CSS for this project.

### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more than 5 linter errors. Project team makes large infrequent git commits. Project shows a basic understanding of React.

### Testing

* 1 - A valid attempt to test this application was made, but there are obvious gaps, with missing unit tests for Redux and React.

### Redux Architecture

App does not demonstrate mastery of Redux - only storing some info, not utilizing information stored

* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
