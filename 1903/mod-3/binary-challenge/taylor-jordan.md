### Evaluator: Travis Rollins
### Students: Taylor Jordan
### Comments:
* Would have liked to see more commits, branches & PRs
  * Some commits like for functionality or testing could get broken out a little more
  * Only 3 PRs
* Good work with the README
* Good work with propTypes.  Would also include propTypes for your mapDispatchToProps as well.  For example in your `Details` container.
* There are lots of linter errors.
  * To use the linter in React, add this line to the script
    * `"lint": "eslint src/"`
  * Shouldn't need to install a new linter, React already has one built in.
* Nice work keeping store flat and removing any duplicate data.
* Would like to see some dynamic routing.
* Good work testing mapStateToProps on `AstroSign`
* I like how you broke out some of the functions in the `Horoscope Form`
* Good testing on apiCalls, actions, & reducers
  * Would recommend breaking out tests for reducers just like you did with the implementation
* Nice component testing with the `Horoscope Form`, testing out changes in state and mocking out events
* Cheers to the 404 page
* For routes, would recommend using the `component` attribute instead of `render` if you don't need to pass props.

## Rubric

### Specification Adherence

* 4 - All requirements from 3 are met. The application completes all iterations above and implements one or more of the extensions. And the evaluator has no recommendations for design changes.
* 3 - The application uses the above technologies to a professional level. The evaluator has minimal recommendations for refactoring or design changes.

### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more than 5 linter errors. Project team makes large infrequent git commits. Project shows a basic understanding of React.
* 1 - PropTypes are substantially unused, README is incomplete, wireframes were not used, or more than 10 linter errors are present. Git history does not show evolution of project, with many large and inconsistent commits. Project shows little understanding of React and significant refactoring is required.

### Testing

* 4 - All requirements from 3 met, all async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).

### Redux Architecture

* 4 - All requirements from 3 met, and no duplication of data exists in the store. Data in the store remains flat (not nested).

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
