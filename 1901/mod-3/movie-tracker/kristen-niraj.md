### Evaluator: Leta
### Students: Kristen, Niroz
### Comments:

3 out of 5 rubric sections are in a failing state.

The UI around the login is confusing without error or success indicators, and user is not automatically routed to where they need to go.

Favorites functionality is a bit buggy.

65 commits is not enough for a project of this size. This indicates that the changesets in a single commit are too large.

Some of the items in the components folder are containers and should be moved.

Most actions and reducers tests in place. No component or container testing in place. No asynchronous tests in place.

Overall architecture of Redux can use work (containers in wrong folder).

## Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. Evaluator has multiple recommendations for design changes.

### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more than 5 linter errors. Project team makes large infrequent git commits. Project shows a basic understanding of React.

### Testing

* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test async functionality was made.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
