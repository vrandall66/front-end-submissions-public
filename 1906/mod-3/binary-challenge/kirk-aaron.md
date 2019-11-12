### Evaluator: Travis Rollins
### Students: Kirk Aaron Veitch
### Comments:

**Project Professionalism**
* Great number of commits and keeping commit messages descriptive
  * Could have more branches and make them a bit more specific.  (one branch is `fetch` and another is `fetching`).
* Good work having a live site up and ready.
* Excellent work with README including setup, tech used, images, and wireframes.  Also good work using a project management tool.
  * Project management tool could get a bit more broken up like testing, but good start with it.
* Also good work keeping linter problems down.  Just a couple in the `helper.js` file.

**Specification Adherence**
* Good work taking in so many options and getting them to display connections.  Having the differnt form options are helpful.
  * Many scenarios where it stays as `Please be patient we're finding flights for you...`.  Think it could be more helpful to say there are no flights available currently.
* Pictures of places to see are cool.  Would be nice to have some extra details on that. 
* Could be interesting to set it so each person can arrive at different times.
  * Also a user likely shouldn't be able to grab a previous date that has already passed on the calendar.  Same for `coming back` should always be after `leaving on`.  Could be fun to look into how you could achieve this?
* Would like to see some kind of errorMsg if something breaks or loading icon.
* Could be nice when displaying the various possibilities to group them by date.
  * If multiple trips exist on the same date, maybe that is a way to categorize them?
  * Also maybe a separate section for locations to visit there instead of the long scroll effect.

**React Architecture**
* Do not need to have the `e.preventDefault` and `e.stopPropagation` on `handleSubmit` in Form.
* `handleSubmit` is pretty busy.  A lot of actions for a lot of properties.
  * Maybe fire one action for `me` and another for `you` setting an object with the related properties?
* Unsure why you are using something like `Let&apos;s Go!` in button when you can use `Let's go`.
* Remember to do something with errors other than console.logging them in `try/catch`.
* Would look into how you can refactor the Trip component.
  * Notice meFlights and youFlights are very similar?  Could you create a component and pass in the data necessary?
* Good work checking if response is okay in fetches.
* Good work breaking out helper functions.  Might break out cleanFlightData even more.
  * Interested to hear about how you figured out the functionality of formating the dates.
* Good work including propTypes.


**Redux Architecture**
* Would like to see an `errorMsg` or `isLoading` property in the store.
* Is it necessary to include properties like `cityName`, `destination`, `meStart`, and `youStart`?  (also startDate and returnDate)
  * Feel like a lot of this is needed in just the Form and is not necessary to keep in store.
* Actions and reducers look good.
* Good work keeping containers inside of containers directory.

**Routing**
* Good work setting it so that the user can go back to the home page.
  * Might be nice to add some kind of hover effect so that the user knows it is an option to click it.
* Would look into how you can create a 404 page if a route doesn't exist.
* Do not need so many `Links` around the App part for the navigation.  One will suffice wrapped around all of it.

**Testing**
* Would recommend having reducer tests broken out just like files.
* Great number of tests overall
  * Good work testing out your actions and reducers
  * Good work testing state changes and simulating events in the Form.
  * Appreciate the number of tests for mapStateToProps and mapDispatchToProps.
  * Good work testing the different snapshot tests as well.
* For apiCalls, missing one more sad path test if the Promise.rejects like if the server is down.
* Would recommend in the future to test out helper files as well.

## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.
* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.
* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 4 - All async functionality is tested.   Asynchronous tests cover happy paths as well as multiple sad paths.  All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.