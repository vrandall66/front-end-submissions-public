### Evaluator: Aidan McKay
### Students: Travis Rollins
### Comments:
* Only one push up to master, no PRs is not professional.
  * Also still not many commits.  Could have more added.
  * No README
* Cheers to having propTypes and not many linter errors
* No 404 page
* Missing an `error` and `isLoading` in store
  - Throws an error but does nothing with it
* Can click characters, but nothing renders on route
  * Have links to each one, but routes are not set up to display anything
* Minimal styling
* Would be nice to have an active state on each tab.
* `Character.js` unfinished
* Methods in `CharacterContainer` like waterNation, fireNation, etc. are very repetive.
  - Use one method and pass in the argument it needs to filter
* Tests could be better for `CharacterContainer`. Testing that that the length is 1 is a good start, but we want to make sure it is filtering correctly.
  - Missing a test to make sure that the correct function is getting fired when clicking on each img.
* Should have more properties in mockState on line 58 in `CharacterContainer` to test that mapStateToProps is giving back the object we expect
* Cheers to testing actions, reducers, & apiCalls
* Overall, unfinished project

## Rubric

### Specification Adherence

* 1 - The application is missing multiple features outlined above. Developer did minimal to no CSS for this project.

### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more than 5 linter errors. Project team makes large infrequent git commits. Project shows a basic understanding of React.
* 1 - PropTypes are substantially unused, README is incomplete, wireframes were not used, or more than 10 linter errors are present. Git history does not show evolution of project, with many large and inconsistent commits. Project shows little understanding of React and significant refactoring is required.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test async functionality was made.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 1 - Application uses React Router, but does not render/use all routes.
