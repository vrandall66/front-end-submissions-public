### Evaluator: Leta
### Students: Evan
### Comments:

* OH NO! Don't commit your API key, EVER! The file should be gitignored
* Link to airbnb breaks - gotta include the "https" at the front of the link href :)
* No 404 handling, but app does not error out, either!
* Redundant data in the store (current apartment should just be the ID)
* App is a container - should move out of the components folder
* With tests for components that conditionally render things, you should test all the states. Example: Overview should be tested with a hood, and without a hood
* Otherwise, lots of good tests here! Component methods, snapshots, async, redux.

## Rubric

### Specification Adherence

* 3 - The application uses the above technologies to a professional level. The evaluator has minimal recommendations for refactoring or design changes.

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
