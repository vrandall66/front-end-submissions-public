### Evaluator: Leta & Travis
### Students: Anneke, Steve, Kevin
### Comments:

* Nice job on overall functionality
* Keep the store flat (romanceMovies and popularMovies should be a single array and the cleaner should add a genre to each film object)
* Keep the store non-redundant (store favorited movie IDs, not the whole object)
* Make sure to keep files organized - if it's a container, it should be inside containers. Looks real unprofessional if they're not organized - it's low hanging fruit so just do it!
* Be consistent (using bindActionCreators vs the longhand way)
* Hooray proptypes!
* Redux testing is great!
* Great job on component tests - all functions seem to be tested, not just snapshots :)
* Had error handling in place :)

## Rubric

### Specification Adherence

* 4 - All requirements from 3 are met. The application completes all iterations above and implements one or  more of the extensions. And the evaluator has no recommendations for design changes.
* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 4 - All requirements from 3 met, codebase has zero linter errors/warnings and readme contains screenshots of application. Project team uses a rebase workflow, taking advantage of github issues to track work. Project shows a complete mastery of React architecture.

### Testing

* 4 - All requirements from 3 met, all async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
