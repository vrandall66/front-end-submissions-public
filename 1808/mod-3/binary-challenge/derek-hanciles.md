### Evaluator: Christie 
### Students: Derek
### Comments: Testing is lacking

## Rubric

### Specification Adherence

* 4 - All requirements from 3 are met. The application completes all iterations above and implements one or
  more of the extensions. And the evaluator has no recommendations for design changes.
* 3 - The application uses the above technologies to a professional level. The
  evaluator has minimal recommendations for refactoring or design changes.
* 2 - The application is in a usable state, but is missing part of one or more of the
  technologies outlined above. Evaluator has multiple recommendations for design
  changes.
* 1 - The application is missing multiple features outlined above. Developer did
  minimal to no CSS for this project.

  [10 Essential Usability Guidelines.](https://speckyboy.com/10-essential-web-application-usability-guidelines/)

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter
  errors, README has been updated with all group members. Project utilized
  wireframes from the outset. All git commits are atomic, made first to
  branches, and use descriptive and consise commit messages. Project
  demonstrates a fundamental understanding of React architecture.
* 2 - Project is missing PropTypes, README updates, wireframes, or has more
  than 5 linter errors. Project team makes large infrequent git commits.
  Project shows a basic understanding of React.
* 1 - PropTypes are substantially unused, README is incomplete, wireframes were
  not used, or more than 10 linter errors are present. Git history does not show
  evolution of project, with many large and inconsistent commits. Project shows
  little understanding of React and significant refactoring is required.

### Testing

* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test
  async functionality was made.

### Redux Architecture

* 4 - All requirements from 3 met, and no duplication of data exists in the
  store. Data in the store remains flat (not nested).
* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.
* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.
* 1 - Application state is mostly outside the control of Redux. Application did not make use of Redux actions and reducers to mutate state. Components do not demonstrate a clear understanding of stateful vs. statelessness.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
* 2 - Application uses React Router, but does not display the appropriate components upon navigating.
* 1 - Application uses React Router, but does not render/use all routes.
