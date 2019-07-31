### Evaluator: Travis Rollins
### Students: Ryan Flachman
### Comments:
* Would like to have seen more commits and PRs
  * commits can get broken out into smaller pieces
  * commit messages could be a bit more detailed
* No README and also no propTypes
* Cheers to having a 404 page
* Lots of buttons that don't appear to do anything.
* Nice dynamic routing for each of the pokemon.
* Would be nice to have a loading img when waiting for next set of pokemon to appear.
* Several parts unfinished, but great start.
* Store doesn't appear to have any redundant data
* Good tests with actions, reducers
  * Would recommend breaking out tests for reducers just like you did with the implementation code
* Missing a number of tests with apiCalls
  * Missing sad path tests as well as test for getPokemonByName
* Nice work implementing thunks and testing them
* Why is GameContainer a `class component` and using `connect` when it doesn't need it?
  * Same for ItemContainer, it does not need to be a container the way it is set up
* Lots of places where you have an `offset` & `category`, would recommend utilizing store instead of having state in so many components.
* Good tests in `ItemContainer` and testing changes in state.
  * Could have some tests to check if a function is run with simulating a click.
* Likely don't need to get all data when the app starts.  Fetch it when you need it.
* Missing tests for mapStatetoProps & mapDispatchToProps
* Solid handling of routes, could refactor to map through or set up another dynamic route for games, pokemon, items, moves, etc.
  * Example: `/:pokemon-query`


## Rubric

### Specification Adherence

* 3 - The application uses the above technologies to a professional level. The evaluator has minimal recommendations for refactoring or design changes.

### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more than 5 linter errors. Project team makes large infrequent git commits. Project shows a basic understanding of React.
* 1 - PropTypes are substantially unused, README is incomplete, wireframes were not used, or more than 10 linter errors are present. Git history does not show evolution of project, with many large and inconsistent commits. Project shows little understanding of React and significant refactoring is required.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test async functionality was made.

### Redux Architecture

* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.

### Routing

* 4 - All requirements from 3 met, and always chooses the correct component for rendering, as well as the correct Route API. Application should account for undefined routes.
