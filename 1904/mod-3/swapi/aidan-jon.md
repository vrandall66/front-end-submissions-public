### Evaluator: Travis Rollins
### Students: Aidan & Jon
### Comments:
* Love the movie music.  And the idea of being able to stop the sound.
  * Might move the `Stop Audio` button higher so it's easier to find for the user.
* Good routing and path handling
  * Excellent work having a 404 page.  Might not show the movie script at that point (just the error page)
  * Might have the `Show Movie Stuff` go back to the `/` route
* Would recommend not fetching all data on the componentDidMount  
  * Although most of the data had loaded when I got there, could cause some performance issues on a slow connection.  Load the data when a user clicks on a button.
* A lot of unneccessary methods like hideLanding, showLanding, setMovie, setPeople, etc.
  * Call `setState` when you need to.
* Gets a bit tricky with setting an array of arrays with data.  Recommend array of objects (so you don't have to be so explict with indexes)
  * Likely shouldn't need a favorites array in state at all.  Add a property to your objects in vehicles, planets, & people to keep track of favoriting.
* Should start default state with the exact data type that you expect to replace it with.  
  * `filmData` starts as an array and then is updated to be an object.
* I appreciate the setting of state with the error.  Now remember to render it! 
* Could do some refactoring with routes in render of `App`.
  * How could `planets`, `vehicles`, `people`, and even `favorites` be rendered using a dynamic route.  Or using an array prototype method?
* Likely don't need a component for one line of text.
  * Such as `Home` or `NotFound`
* Lines 12-15 on `Card` could get refactored.  Aside from the src, they are exactly the same.
  * Use a ternary or something for the logic of src, assign it to a variable, and assign the variable to the src
* Nice work separating your cleaner functions and fetches into separate files.
* A few failing snapshot tests to double check on
  * Would have two snapshot tests for the `Card` component to check for the image source of the favorite image.
* Would like you to continue working on the tests for the routes.  Make sure you have everything you need imported.
* Good work writing tests for methods in `App` and changes in state.
* Good work testing cleaner functions as well as your apiCalls!
  * Shouldn't need `async/await` when doing something like `expect().rejects`
  * Would like to see both `sad path` tests
* Next, add some tests for your `componentDidMount` and make sure your methods are getting called.
* Cheers to including propTypes!
* Great work on your README
* Good work with commits and branches.  Might be a bit more specific with commit messages
* Saw a few short messages on PRs, but would like to see more
  * Leave code reviews and comments on code.  Leave a papertrail to show your GH workflow.
* Nice work with no linter errors aside form the `iframe`
* Did you use a Trello board?  Can I see it?  Include it in your README

## SwapiBox Rubric

### Specification Adherence

* 4 - The application completes all iterations above and implements one or more of the extensions.  The evaluator has no recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 


### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.

### Testing

* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.