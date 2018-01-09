# SWapi-Box Eval

### Evaluator:
### Students:
### Comments:
- App test needs to mock the fetch because disabling the lifecyle functions is causing
 the component not to mount which is crucial to the interaction of your application
  - some tests are relaying on network requests. This should be mocked.
  - clicked category can be refactored into a higher order function that will not make an api call every click, but check the length to see if it's already in state. you can also pass in
- Controls should just use an active class

## Rubric

### Specification Adherence

3 - The application completes all 4 iterations.

### Code Quality

3.5 - Developer appears comfortable in React. There are minor opportunities to refactor.

### CSS/Design

3 - Developer has made a targeted effort to make the app appealing and user friendly. Evaluator has multiple recommendations for design changes. Follows majority of the 10 Essential Usability Guidelines.

### Testing

3 - Almost all components are tested to a level that indicates developer has an understanding of testing

### PropType Implementation

Pass - Proptype validation is implemented for any component receiving props.

### Code Sanitation

The output from ESLint shows…

4 - Zero complaints

### Workflow

4 - Developer(s) make many small, atomic commits that clearly document the evolution of the application and do not contain irrelevant changesets that aren’t reflected by the commit message. Commit messages are concise and consistent in syntax and tense. Developer(s) effectively use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing directly to master. There are no instances where the developer(s) have committed source code that should be .gitignored. There are no instances of “dead” or commented-out code and debugger statements like console.log.
