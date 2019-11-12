### Evaluator: Travis Rollins
### Students: Michael Schneider
### Comments:

**Project Professionalism**
* Great amount of commits and branches.
  * Good work being consistent with descriptions for commits and branches.
* Cheers to having some issues at the end and sticking with a GH project.
* Well done with your README including setup, tech used, link to your profile, images, and testing suite.  
  * Might also include wireframes here.
* A few syntax errors in the linter, but not too bad.

**Specification Adherence**
* This application is hilarious.
* Might either give a notification or categorize each set of supplies if you only want the user to be able to select one from each category.
* Rockets route could be styled a bit more to make use of page.
* Could be nice to click a proposal from before to view information on it again and why it was rejected.
* Would imagine if I logout and then login with a different name, proposals wouldn't display from before.
* Might have a label around each supply so I can click the entire thing and select it, instead of clicking the dot.  (just for accessibility)

**React Architecture**
* Don't think the `e.stopPropagation` is necessary in the `Welcome`.
* Good work with apiCall and checking if property is ok.
* Careful having functions inside of functional components.  Unable to test them as a result.
* Great work including a `try/catch` in componentDidMount.
  * Make sure to do something with error for catch.  Console.log is not helpful for the user.
* Might movie the `cleanRockets` function out of `componentDidMount` to make it easier to test.
* Good work keeping logic out of return statements.
* Good work including propTypes.
  * Make sure they are up to date.  In some scenarios like in the `Welcome` container, you aren't using the `name` from props.

**Redux Architecture**
* Store is pretty clean.
* I might move payloads into a different section of the store since there are places where duplicate data for that exist nested.
* Would recommend having an `errorMsg` and `isLoading` property in the store as well.
* Great work with your actions and reducers.
  * Proposals reducer starts to get a bit long.  I wonder if it would help clean up the logic if you have a property for `proposalInProgress` and then another property for `finalizedProposals` so you don't have to map through every time.

**Routing**
* For overview of a proposal, I might make the route dynamic to include the id like `/overview/:overview_id`.  That way you can share the link to another person.
* Good work with routing and making it very clean and accessible.
  * Could be nice to have a back button if I wanted to change my supplies after submitting.
* Look into how you could create a 404 page if route doesn't exist.
* Might look into how you can refactor the `routes` in your App.  All relatively similar.  Maybe have an array and map through returning the `Route` component.
* Some good places using the `Redirect` component.

**Testing**
* Good work testing actions and reducers.
* Good work testing all happy and sad paths for the apiCall.
* Good work testing the method and mockDispatchToProps in App.
  * Would have liked to seen a test for your `componentDidMount`.
  * Would like to have some tests for methods in for `mapStateToProps` and `mapDispatchToProps` and methods for `Overview` component.
  * Same for Rockets component as well and checking changes in state as well as simulating events.

*Update*
* Excellent work adding some more tests for components hooked to the store including `mapStateToProps` and `mapDispatchToProps`.
  * In a test like `Rocket.test.js`, can test both properties in the same test.  The idea of this function is to only return certain properties out of the store.  So you can pass the entire store through, but only expect it to have a `proposals` and `rockets` property.
* Some really good examples of React unit tests like event simulations and changes in state like the `Rocket.test.js`.

## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.
* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  

### Redux Architecture

* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.
* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 4 - All async functionality is tested.   Asynchronous tests cover happy paths as well as multiple sad paths.  All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.