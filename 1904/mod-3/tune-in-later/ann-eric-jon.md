### Evaluator: Travis Rollins
### Students: Ann & Eric & Jon
### Comments:
* Good work only having 2 linter errors.
* Good work on README including images and group members. I would recommend including also `wireframes`. 
  * Noticed that GH Projects hadn't been updated in several days.
  * Good work starting to do GH issues.  Would recommend sticking to a template for each one and giving additional details under the description.
* Keep an eye on [number of commits](https://github.com/eoneill23/tune_in_later/pulse) (as well as [contribution to code](https://github.com/eoneill23/tune_in_later/graphs/contributors)).
* Great number of commits.  Commit messages are well done.  Might continue on being as specific as possible such as [snapshot tests](https://github.com/eoneill23/tune_in_later/commit/bdaefb723af2b3f02af51cea7f6bdf58a52e6ba3).  We likely want to mention what we snapshot tested.
* Would like to see more helpful code reviews on PRs like [this one](https://github.com/eoneill23/tune_in_later/pull/39).  While I appreciate the gesture, `Good/Great job` isn't the most helpful.
* Loving the retro vibe of the site.
  * Might play around a bit with spacing of elements
  * Hovers make other icons move ever so slightly
  * Might make buttons look a bit more like buttons 
* Good error handling if user hasn't signed in yet and tries to favorite a card.
* Love that when I sign up, it automatically signs me in as well.
* Good work with error handling on forms for signing up and signing in.
* Might include a message if there are no favorites and I go there.
* Would highly recommend not using `window.location.reload()`.  Clear out the reducer for your user.
* Good work with dynamic routing.  Would recommend filling up the space a bit more with a bigger image and style the layout.
  * Might include a 404 page for a route that doesn't exist
* Nice clean actions.  A few names that I could rename as more of an "action".
  * Similar to `addAlbums`, have a verb for `validUser` and `invalidUser`
* Good work separating containers and moving them into their own folder.
* Super clean reducers.  Store is very flat and no duplicate data.
* Header in `App` likely could get broken out into it's own component.  
* With routes like `/signup`, `/`, `/login` why not use Component?
  * Also noticed you have the same route `/` twice.  You can use it once, and include both necessary components.
* When passing props, if you want to pass all of the data included you can do `<CardDetails {...foundAlbum} />`
* Good work adding propTypes
* Would highly recommend moving functions out of functional components like `Card.js`.
  * Unable to test them as a result.
  * Might also recommend instead of passing each prop down individually for your `Card`, pass down an object as a prop for all things relating to your album.
* Many similarities between all three forms.  How could some parts get refactored/reused like your methods?
  * Pass down methods that need to get run as props.  Then you only need to test them once.
* FANTASTIC number of tests ya'll!
  * Solid tests for your apiCalls.
  * Great reducer tests for default state and including types.
  * Good work on tests for your actions.
  * Good examples of tests for mapStatetoProps and mapDispatchToProps in `Form`. 
  * Also good work with the tests for changes in state and event simulations in `Form`.
    * Will need to do mockImplementation on `deleteUser` in `Card.test.js` in order to tell it to return a Promise that resolves into some data.  (this is because you are calling `.then` in the actual code, but currently it is just a mock function).

## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.
* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 
* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.
* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Redux Architecture

* 4 - All requirements from 3 met, and no duplication of data exists in the
  store. Data in the store remains flat (not nested).

### Testing

* 4 - All async functionality is tested.   Asynchronous tests cover happy paths as well as multiple sad paths.  All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.