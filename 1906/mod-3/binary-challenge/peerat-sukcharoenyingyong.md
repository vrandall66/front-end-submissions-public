### Evaluator: Travis Rollins
### Students: Peerat Sukcharoenyingyong
### Comments:

**Project Professionalism**
* Good number of commits and start to branches.
  * Good work being consistent with descriptive commits
  * Keep branches specific as well (something like `more-testing` and `more-testing2` isn't clear)
* Cheers to the issues you added and labeling them as well.
* Remember to use a project management tool even when working solo on a project.
* Good work with README including description, tech used, & screenshots.
  * I would be a bit more clear on the setup and would also recommend including wireframes.
* Quite a lot of linter warnings.  Remember to include this script, `"lint": "eslint src/"` inside of your package.json under the scripts object.  Then run `npm run lint`.

**Specification Adherence**
* In the future, make sure that a user does not have to install an extension in order to get data. (if there are CORS issues, either find another way to get around it or use different api)
* GetWeather is broken because it cannot map through cities.
  * Current conditions and future outlook are also broken.
  * Realized later that I need to click `Send All Station Data` in order for this to work but not a great UX.  Alerts are not great either to tell user that data is in store.  
* Able to press `Get Weather` button but app breaks because of handling of errors
* Fetches are not dynamic, only can look up places with `San` in it.
* Typing in latitude/longitude breaks the app.
* Completely missing catches to handle if app breaks.
* Good work displaying different backgrounds depending on weather condition.
* Some colors feel a bit more random.  Could work together more.

**React Architecture**
* No need for `CustomList` to be a class component. 
  * Also code gets very messy here.  Keep logic out of return statement. Definitely some refactoring that could happen here.
* A ton of console.logs need to be cleaned up.
* Remember to be consistent always checking if the response is ok before doing `response.json` like in `fetchUsingStationID`.
* WeatherCard needs a ton of cleanup.
* `Weather`, `CustomList`, and `Favorites` components likely do not need to be a class component.
  * Not keeping track of state.  Move the method into a parent component and pass it down as a prop.
* Variables like `x` in the `Form` does not display developer empathy.  Hard to know what you are keeping track of here.
* Good work including propTypes for props from components and store.
* Remember to keep components and `containers` in their specific directories.
* A lot of methods imported in componets like `App` like the api calls that are also unused.

**Redux Architecture**
* Some actions/reducers unused like `favorites`.
* Would like to see you keep track of `isLoading` and `errorMsg` properties inside of the store.
* Actions and reducers are set up fine.
* Some components have access to props from store that are not necessary like in `App` with the "cities" and "stationIDs".
  * Same for `CustomList`, only weatherData is needed.
* Good work using mapDispatchToProps where needed.

**Routing**
* Good work using `component` and `render` when necessary on Routes.
* Several broken routes unless user follows through an exact way.
* Good work making routes available at all times.

**Testing**
* Missing tests for actions and reducers.
* Good start with testing apiCalls but missing sad path tests in them.
  * Also check that one of the tests is silently failing.
* Good work with the test for `mapDispatchToProps` in the Form.  Now test the rest of them.  Same for `mapStateToProps`.
* Would like to see some tests for async methods.
* Currently not having any passing event simulating tests or changes in state.

## Rubric 

### Specification Adherence

* 1 - The application is missing multiple features outlined above and in it's current state is non-functioning. Developer did minimal to no CSS for this project.
* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 

### React Architecture

* 1 - PropTypes are substantially unused. Project shows little understanding of React and significant refactoring is required including but not limited to component structure, knowing when to use class vs functional components, mutation of props, or etc.  Unneccessary data is being passed down to child components through props. File structure is not modular.
* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  

### Redux Architecture

* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.
* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 1 - A valid attempt to test this application was made, but there are obvious gaps with missing unit tests for Redux and React.  

### Routing

* 1 - Application uses React Router, but does not render/use all routes according to spec. Application does not utilize built in React Router components and manipulates history instead.  UX is challenging and frustrating where multiple pages on the application are missing links to routes.
* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.