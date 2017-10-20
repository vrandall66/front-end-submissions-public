# SWapi-Box Eval

### Evaluator: Limbo
### Students: Hector Sanchez, Robbie Greiner
### Comments:
* Need to mimic ALL data exactly as your app expects to receive it
  * Every time you have a fetch call, mimic the exact data it gets back in the body (after the res.json())
  * Need to also have a fetchMock for EVERY url that will get pinged in your tests

## Rubric

### Specification Adherence

4 - The application completes all 4 iterations above and implements one or more of the extensions.

### Code Quality

3 - Developer appears comfortable in React. There are minor opportunities to refactor.

### CSS/Design

3.5 - Developer has made a targeted effort to make the app appealing and user friendly. Evaluator has multiple recommendations for design changes. Follows majority of the 10 Essential Usability Guidelines.

### Testing

3 - Almost all components are tested to a level that indicates developer has an understanding of testing

### PropType Implementation

Pass - Proptype validation is implemented for any component receiving props.

### Code Sanitation

The output from ESLint shows…

4 - Zero complaints

### Workflow

3.5 - Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of “dead” or commented-out code and debugger statements like console.log that need to be cleaned up.
