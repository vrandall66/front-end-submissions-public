### Evaluator: Travis Rollins
### Students: Kate Malone
### Comments:

**Project Professionalism**
* Would like to have more commits and branches.
  * Some commits could be a bit more specific like [fetching data](https://github.com/katemalone/travel-planner/commit/c477f8457e99e9870405c3a22ef41ad3805a7d6f)
* Noticed some changes were made to GH Projects around 9 PM.  Make sure to adjust it as you go along.
* Also noticing a styling commit after 9 as well. These were not included during grading.
* Appreciate including a description for the README.  `Getting Started` could be set up a bit better with each step to get it running.  
  * Good work including tech used (likely don't need to include CSS), data flow, and image of app.
  * Remember to include wireframes as well.
* A few linter errors but not too bad.  Remember to include a script in your `package.json` to run `npm run lint`.  The script is `"lint": "eslint src/"` and it goes under your script object.

**Specification Adherence**
* Home route looks very nice.  Appreciate the hover effect to know I can click on it.
* Form still needs quite a bit of styling.
  * A bit complex to figure out what the user needs to type in for airport code.
* Submit button takes me nowhere even though it is updating the store.

**React Architecture**
* Good work keeping components and containers in their respective directories.
* `randomizeInternatal and domesticCity` inside of `UserForm` are exactly the same.
  * Variables are very confusing.  What does each number stand for?
  * Also noticing the exact same function in the `helpers`.
  * What is the purpose of the `event` for these two functions?
* I would have callbacks for the Form be consistent.  (noticing some anomyous and others are setting it)
* Confused why `getFlightOptions` is a method in App when it needs to be used in the component.
  * Good work using `try/catch` here and doing something with error message.
  * Alot of refactoring could happen with all of the methods being invoked and mapping through similar pieces of data.  How could this refactored so it just maps through once.
* Missing propTypes.
* Good work breaking out apiCalls but think the url should exist in the apiCalls as well.  Pass the `flightObj` through when invoking `getFlights` and include it in the url there.
  * Appreciate the check of the property ok to make sure the response is good.
* Confused as to having all of the imports in the `LoginForm`.
* Currently `setBooking` is a prop that is not used in the App.
  * Same with `errorMsg`.

**Redux Architecture**
* Good work having `isLoading` and `errorMsg` properties.
* Unsure what the `bookings` array is for currently.
* Actions and reducers look good.
* Confused on the purpose of returning `sendIt` from `componentDidMount`.  Should be accessing it from global state.
* mapStateToProps and mapDispatchToProps look good in `App`.


**Routing**
* Do not need to use `render` prop for `LandingPage` in App since it does pass props.  You can use `component`.

**Testing**
* Only testing one of the actions.
* Testing default state for reducers, but missing tests for some reducers if the action has a type.
* Good start with testing the apiCall, but missing tests for happy path on what it returns and a sad path test if the fetch rejects (such as the server is down).
* For all of the helper functions, I would recommend including tests for those as well.
* Confused what the beforeEach is for in `App.test.js`.
  * Good snapshot test and testing `mapStateToProps` and `mapDispatchToProps`.
  * Would love to see a test for `getFlightOptions` to check that the correct methods get fired.
* Good tests with `Form` component testing changes in state.
  * One good example of simulating an event for a test.  Would like to see more.
  * Would love to have tests for `handleMonth` and the `randomize` functions.

## Rubric 

### Specification Adherence

* 1 - The application is missing multiple features outlined above and in it's current state is non-functioning. Developer did minimal to no CSS for this project.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 

### React Architecture

* 1 - PropTypes are substantially unused. Project shows little understanding of React and significant refactoring is required including but not limited to component structure, knowing when to use class vs functional components, mutation of props, or etc.  Unneccessary data is being passed down to child components through props. File structure is not modular.
* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  

### Redux Architecture

* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.

### Testing

* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods.  All routes have been tested as well including dynamic routes.  There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps.  No attempt to test async functionality was made.
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 1 - Application uses React Router, but does not render/use all routes according to spec. Application does not utilize built in React Router components and manipulates history instead.  UX is challenging and frustrating where multiple pages on the application are missing links to routes.
* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.