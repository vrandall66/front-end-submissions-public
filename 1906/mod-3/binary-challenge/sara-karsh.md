### Evaluator: Travis Rollins
### Students: Sara Karsh
### Comments:

**Project Professionalism**
* Good amount of commits but would like to have more branches.
  * Appreciate specific branches and consistent commits.
* Great work with the README having the table of contents with tech used, screenshots, how to setup, and how the app should work. 
  * Could be good to also have wireframes?
* Good work sticking with GH projects and implementing that.
* Quite a number of linter warnings/errors.  Remember to include the script `"lint": "eslint src/" ` inside of package.json under the scripts object and run `npm run lint` in terminal.

**Specification Adherence**
* Super cool to be able to add all of the different characters and pieces together.
* Love to see the movies and get data on those as well.
* And then submitting that information to get a score back.
* Appreciate the submit button doesn't work or break until everything is filled out (good work adding extra details on what to do)
* Cool hover effect around buttons.  Might make them still look a little like a button so it's easier to see as opposed to it just being text.

**React Architecture**
* Great work being consistent and always checking that the response is okay in all fetches before doing `response.json`.
* Might move some of the cleaning functions out of apiCalls like `fetchFilms` just so that they are easier to test later on.  
  * Can move then into a helpers directory and cleaners file.
* Great work keeping components and containers in their respective directories.
* Excellent work implementing propTypes and keeping components clean.
* Could be interesting to see if you could refactor Nav so you map through an array and return Links for each one.
* Great work implementing try/catch and doing something with error if it hits the catch in `App`.

**Redux Architecture**
* Appreciate keeping track of `error` inside of the store.  Would also like to see it keep track of loading.
* Rest of the looks clean and no duplicate data.
* Good work with actions and reducers.
* Good work implementing mapStateToProps and mapDispatchToProps where necessary.

**Routing**
* Great work with routing and making all routes accessible at any point.
* Routes always render the correct component.
* Might look into how you can create a 404 page if a route doesn't exist.
* Some of the Route components, you can use `component` instead of `render` prop if you just want to render the component and don't need to do extra logic or pass props.

**Testing**
* Great work testing out your actions and reducers. (including tests for defaults and if the action has a type).
* Good work testing apiCalls.  Remember to test that the correct url was called as well.
  * Nice work testing multiple sad paths.  A few that are failing silently.  Would check the error and why it's doing that.
* Good work testing that `fetchFilms` was called on componentDidMount of App.  Check the other methods as well.
* Great work testing the methods in the `App` as well along with `mapStateToProps` and `mapDispatchToProps`.
* Might include a test on `CharacterCard` simulating an event of clicking on the button and checking that `toggleAddCharacter` was called.

## Rubric 

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.
* 4 - The application completes all iterations above and implements one or more of the extensions.  The evaluator has no recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 
* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 4 - All async functionality is tested.   Asynchronous tests cover happy paths as well as multiple sad paths.  All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.