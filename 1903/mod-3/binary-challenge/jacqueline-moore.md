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


## Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the technologies outlined above. Evaluator has multiple recommendations for design changes.

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
