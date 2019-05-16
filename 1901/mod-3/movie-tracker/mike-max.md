### Evaluator: Will
### Students: Mike, Max
### Comments:

Your reducers should not have verbs in them. It should reflect the name of the piece of the global store they interact with. For example, instead of "addTopMoviesReducer", it should be "moviesReducer" or possibly "topMoviesReducer". Reducers should all be able to do more than one thing, so should not be named to limit them to one thing.

Some components/containers have conditional rendering in them, yet you only have one snapshot test. You should have snapshots to capture each potential outcome of the component/container.

## Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal
  recommendations for design changes.

### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more
  than 5 linter errors. Project team makes large infrequent git commits.
  Project shows a basic understanding of React.

### Testing (PENDING)

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 4 - All requirements from 3 met, and always chooses the correct component for
  rendering, as well as the correct Route API. Application should account for
  undefined routes.
