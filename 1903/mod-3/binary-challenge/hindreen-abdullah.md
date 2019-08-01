### Evaluator: Leta
### Students: Hindreen
### Comments:

* Nice job sticking to your MVP
* Hard to tell but it looks like the info in the store is flat and non-redundant
* Information is a LITTLE sparse, but it's all explained
* Good job adding dynamic routing
* 404 handling in place
* Some bugs come up with the date functionality
* Don't do multi-line ternaries, EVER!
* Take logic out of renders/returns
* Missing component method tests from containers - must test more than just snapshot and mapStateToProps/mapDispatchToProps
* Missing tests for actions
* Your API key should NEVER be added to github. Should have been placed in a gitignored file and imported into your apiCalls file
* No PropTypes used

PROJECT FAILING
Extension due Thursday @ 9pm:
  - Test all component/container methods
  - Test Redux actions
  - Add PropTypes

AFTER UPDATES, PROJECT IS PASSING

## Rubric

### Specification Adherence

* 3 - The application uses the above technologies to a professional level. The evaluator has minimal recommendations for refactoring or design changes.

### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more than 5 linter errors. Project team makes large infrequent git commits. Project shows a basic understanding of React.

AFTER UPDATES, PASSING

### Testing

* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test async functionality was made.

AFTER UPDATES, PASSING


### Redux Architecture

* 4 - All requirements from 3 met, and no duplication of data exists in the store. Data in the store remains flat (not nested).

### Routing

* 4 - All requirements from 3 met, and always chooses the correct component for rendering, as well as the correct Route API. Application should account for undefined routes.
