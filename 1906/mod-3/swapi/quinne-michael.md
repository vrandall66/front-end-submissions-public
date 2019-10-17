### Evaluator: Robbie
### Students: Quinne and Mike
### Comments:

* Taking a long time to load the characters for each movie...
* The dark theme is really nice, it's simple but very clean
* For each character, is other movies limited to one?
* No way to get back to all movies when you are on the favorites page
* Like the loading animation

* Like how apiCalls are broken out into individual functions- - nice job with `fecthAllCharacterData` and utilizing `Promise.all()`
* The Routes in app are getting a little redundant - `/movies` has a lot of routes - this can be moved to be rending one component (maybe a container) and having conditional rendering within the container if needed
* Why the difference in `/movies/:episode_id` and `/movies/:id` in the routes?
* Why the need for ` this.props = props;` in the Form component
* Overall, the form looks good!
* How did you like the characters being in the `Movie` component state compared to having it all in App?

* 21 tests - some prop type failures at the time of assessment
* Missing some unit testing for `App`
* Form tests look good - what was the trouble with the commented out test?

* Mike, you might want to look at your git config since your commits aren't showing as a true contributor
* Nice job with your Kanban board


## SwapiBox Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Routing

* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.
* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.

* Improvements here could be to reduce redundant routes and use the `match` params where applicable, but a great start into React Router nonetheless

### Testing

* 2 - Nearly all unit tests are in place. Components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods (including `componentDidMount`).  No attempt to test async functionality was made.
* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.
