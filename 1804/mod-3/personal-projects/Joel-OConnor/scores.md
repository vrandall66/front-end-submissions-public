### Project Scope

A good project idea should:

* Break down into logical iterations so that you can deliver a strong product on every check-in
* Be something that real people would want to use to solve a problem
* Have enough *technical* challenge to be worth your time (as opposed to a *content* challenge)

## Rubric

### Specification Adherence

- 4 - The application completes all 2 iterations above and implements one or more of the extensions.
- 3 - The application completes all 2 iterations.
- 2 - The application is in a usable state, but is missing some of the features outlined in the specification above.
- 1 - The application is missing multiple features essential to having a complete application.

### Code Quality

- 4 - Developer demonstrates complete understanding of React with appropriately separated components and exceptionally well refactored code.
- 3 - Developer appears comfortable in React. There are minor opportunities to refactor.
- 2 - Developer selected appropriate libraries and frameworks to build the app but did not use them as intended. Significant refactoring necessary.
- 1 - Developer did not make any effort to use React effectively or refactor code.

### CSS/Design

- 3 - Developer has made a targeted effort to make the app appealing and user friendly. Evaluator has multiple recommendations for design changes. Follows majority of the [10 Essential Usability Guidelines.](https://speckyboy.com/10-essential-web-application-usability-guidelines/)

### SASS/SCSS

- Pass - Styles are written using either SASS or SCSS

### Testing

- 3 - Almost all components are tested to a level that indicates developer has an understanding of testing

### PropType Implementation

- Pass - Proptype validation is implemented for any component receiving props.
- Fail - There are components missing proptype validation.

### README Updates

- Pass - The README.md file has been updated with a description of the project, the team, and how to get it up and
  running

### Code Sanitation

The output from ESLint shows…

* 3 - Five or fewer complaints

### Redux Architecture

* 4: Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data and nothing more. All state changes are handled through Redux actions and reducers.
* 3: At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.
* 2: Application state is mostly outside the control of Redux. Application did not make use of Redux actions and reducers to mutate state. Components do not demonstrate a clear understanding of stateful vs. statelessness.
* 1: Application does not make use of Redux to manage state. There are little or no connected components.

### Routing

* 4: Application is a single page and uses the React Router to display appropriate components based on URL.
* 3: Application is a single page and uses the React Router but does not display the appropriate components upon navigating.
* 2: Application does not render/cannot find additional routes.
* 1: Application did not use a Router

### Workflow

- 4 - Developer(s) make many small, atomic commits that clearly document the evolution of the application and do not contain irrelevant changesets that aren't reflected by the commit message. Commit messages are concise and consistent in syntax and tense. Developer(s) effectively use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing directly to master. There are no instances where the developer(s) have committed source code that should be .gitignored. There are no instances of "dead" or commented-out code and debugger statements like console.log.

