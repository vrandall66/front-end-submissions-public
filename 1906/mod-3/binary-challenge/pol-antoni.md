### Evaluator: Travis Rollins
### Students: Pol Antoni
### Comments:

**Project Professionalism**
* Good amount of commits but would like to see branches other than master.
  * Even though you are working solo, having branches can be nice to have as a sandbox and also can be helpful to have others test things before merging into master.
  * Good work keeping commits descriptive.
* I appreciate the issues you added.
* Would have like to see you use a project management tool even on a solo project.
* Good work with README including a description, setup, tech used (likely don't need to include things like HTML5 or even JavaScript), screenshots, and user.
  * Remember to include wireframes as well.
* A LOT of linter errors.  Remember to include a lint script in your package.json.  The script is `"lint": "eslint src/"` and it goes under your scripts object.  Then run `npm run lint`.


**Specification Adherence**
* Love the filtering of data.  Can be hard to understand what I am actually doing through when moving things around.
  * Maybe have more instructions?
* Slightly difficult to navigate around app without using back button built in browser.
* Clean UI in general. 
  * Could be cool to have background image of planet change based on which one I'm looking at.
* Appreciate errors for the form when it doesn't work.
* Good work using last api for logging in.  Some cool future iterations or favoriting of planets.

**React Architecture**
* Not a huge fan of you using material-ui for this.
  * Think you could have easily built this and made it stand out more without using this.
* Good work with apiCalls and checking of response is ok.
* Where did you get the functionality for filterExoPlanets from?
  * Can you explain it?
* Same for using react hooks in `NavigationBar`
  * Can you explain how this works as well?
* Nice work keeping logic out of return like the `ExoPlanets` container.
* Good work keeping components and containers in correctly directories.  Remember to move over `AccountManager` over to containers.
* Good work using a try/catch in the `componentDidMount` of App.
* Cheers to using propTypes throughout your components.
* Potentially for error for the form, I might keep that in the local state of the login component.  
  * This is because it only relates to the Form.
* For `clearInputs`, mapping through all of the keys is actually causing it to fire `setState` multiple times instead of just once.

**Redux Architecture**
* Good work including properties for `isLoading` and `errorMsg`.
  * Now remember to use them.
* Good work keeping store clean of duplicate data and flat.
* Actions and reducers look solid.
  * Good work having an initialState for the filter.
* Curious as to why you have thunks installed but not using it?
* Not actually using `error` or `isLoading` from store in App. (unnecessary props at this point)
  * Again similar issue for the loginForm with the `isLoading`.

**Routing**
* On login form, missing a route to go back to home page.
* Good work with dynamic routing for each planet.
  * Missing routing to go back to a home page as well after clicking on a plant for more details.
* Good work using a `Redirect` in the login component.
* Not necessary to have so many `Route` components for the root route.  
  * Just need one and then the components you want to render inside of it.
  * Also do not need to use `render` prop for `Route` for components where you are not doing extra logic or passing props.  Can use `component` prop.

**Testing**
* Great work testing your apiCalls.
  * Remember to include another sad path test for if the promise rejects. (such as if the server is down) for `getData`.
  * Good work testing this in the `attemptCreateUser`.  Now include a happy path if everything works well.
* Good work testing your actions and reducers.
* Would love to see a test for your `componentDidMount` in your App.
  * Good work testing `mapStateToProps` and `mapDispatchToProps` in App.
* Careful of nested describe blocks for `ExoPlanetContainer`.
  * Make sure you give a `filters` prop for your React component.  This is why it is breaking.
* Good work with snapshot tests and conditional rendering as in the Login component.
  * Good work testing changes in state in the Login as well as well as simulating events.
* Missing some tests for async methods in components.  Try and give this a shot in the future. 
  * Such as `handClick` in the `Login` component and making sure methods fire.


## Rubric 

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.
* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.
* 4 - All requirements from 3 met, and no duplication of data exists in the store. Data in the store remains flat (not nested).

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.