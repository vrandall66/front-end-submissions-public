### Evaluator: Leta
### Students: Jacqueline
### Comments:

* README is thin
* Descriptive commit messages
* UI is a little confusing - it's unclear which parts of the form the input fields belong to. Could use more separation between sections
* No loading indicator
* No way to get back to search form in order to add more plants
* No 404 handling
* Redux store is unclear - what is `responses`?
* Data in store is redundant
* Many containers are in components folder. A 'container' is any component that is connected to the store (via mapStateToProps or mapDispatchToProps)
* Missing testing for mapStateToProps and mapDispatchToProps
* If you're using thunks they must be tested

PROJECT IS FAILING
Extension due Thursday @ 9pm:
  - Add container tests (mapStateToProps, mapDispatchToProps) for all components/containers that are connected to the store
  - Add PropTypes
  - Add tests for thunks

## Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the technologies outlined above. Evaluator has multiple recommendations for design changes.

### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more than 5 linter errors. Project team makes large infrequent git commits. Project shows a basic understanding of React.

### Testing

* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test async functionality was made.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
