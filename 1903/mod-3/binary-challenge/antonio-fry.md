### Evaluator: Leta
### Students: Antonio
### Comments:

* Good use of PRs
* Commit messages are a bit inconsistent
* console.logs are still hanging out in code
* mapStateToProps test in App.js should start out state with extraneous info, so you can see that the mSTP is only pulling in the specific data you want.
* Several containers are still in the components folder
* FeaturedCharacter should not bring in all the characters - it only needs to know about one
* Overall, very thin use of Redux

None of the pieces are in a terrible state, but overall the app doesn't really show a mastery of the learning concepts in M3. Given that this is kind of a bare-minimum app, we'll need to see a very strong turnout from tomorrow's final assessment.

## Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the technologies outlined above. Evaluator has multiple recommendations for design changes.


### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.
* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
