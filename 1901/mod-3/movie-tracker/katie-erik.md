### Evaluator: Leta
### Students: Katie, Erik
### Comments:

Missing critical functionality (favorites). There are only 76 commits - for a project this size, we'd expect to see upwards of 150.

Reducers should not be named with verbs. They should match the part of state they update. For example, instead of "get NowPlayingReducer", it should be "nowPlayingReducer".

Create a containers folder alongside the components folder, and put your connected components into the containers folder. "Component" and "Container" should not be capitalized; they are not components, they're just folders.

The components are rather confusingly named. From a glance, I don't know the difference in purpose between App, Home, Controls. Those all seem very similar to me.

## Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. Evaluator has multiple recommendations for design changes.

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.

### Testing

* 4 - All requirements from 3 met, all async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
