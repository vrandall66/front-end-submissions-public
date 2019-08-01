### Evaluator: Leta
### Students: Katie
### Comments:

* UI is disappointing
* App does not match the description/title - no speech stuff going on here
* Extension of express server clearly detracted from polishing the app
* FE README is copied from other project and not filled out
* BE README is nonexistent
* FE commit messages are inconsistent
* BE has single commit
* Good use of GH issues - would like to see tags added (MVP, nice to have, bug...)
* No error route handling
* 404 page in place but does not trigger in all cases (ex: `/lists/7`)
* 28 failing tests
* Missing tests that demonstrate changes to state (example: the form component does not test that simulated events are setting the local state)
* Redux store is flat and non-redundant which is good

<!-- PROJECT IS CURRENTLY FAILING -->

<!-- Extension: Thursday @ 9pm
  - Fix tests so they are passing
  - Complete component tests (methods, changes to local state)
  - Write thorough, complete READMEs for both BE and FE applications -->
  
After updates, project is now passing

## Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the technologies outlined above. Evaluator has multiple recommendations for design changes.

### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more than 5 linter errors. Project team makes large infrequent git commits. Project shows a basic understanding of React.

AFTER UPDATE: PASSING


### Testing

FAILED - score can be updated if: tests are fixed and passed, local state changes are tested, component methods are tested

* 4 - All requirements from 3 met, all async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test async functionality was made.
* 1 - A valid attempt to test this application was made, but there are obvious gaps, with missing unit tests for Redux and React.

AFTER UPDATE: PASSING


### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
