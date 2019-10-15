### Evaluator: Travis Rollins
### Students: Brandy Mello
### Comments:
* Could have more commits and details in some commit messages. What are you `cleaning up`?  What `routing issue` was fixed.  Many were descriptive though! 
* Good work with README showing images, gifs, wireframes, descriptions, etc.
* Would like to have seen a project management tool been used.
* Only about 7 linter errors.  Make sure to add `"lint": "eslint src/"` script in to package.json.
* Don't typically recommend scrolling left and right (most apps scroll up and down).
* A few style suggestions
  * Might style the Home & Play Game buttons a bit more to fit in the with the overall style
  * The game scrolls for a very long time.  Might lay it out like a grid. Or add in some pagination?
* Wonder if questions could be organized by difficulty.  Or a hint button for a user who doesn't know the solutions?
  * Careful of scrolling images in a scrollable app.  Double scrolls can create a challenging user experience.
* Love the images and idea of the game though!  Was exciting when I did get a correct answer.
* Would like to see a 404 page for a route that doesn't exist.
* Good work keeping code clean and separating components and containers.
* Excellent work implementing propTypes.
* A little bit of duplicate data storing characters and then characterNames as well.
  * Should need to run the fetch twice for getCharacters in `componentDidMount` in App.  Run it once, and then you have the data, use it to store it/clean it how you need to.
* Good work separating apiCalls
* Would really like you to do something with error message instead of console.logging it.  App breaks otherwise.
* Good start with number of tests, but could be more.  Make sure to update the few failing snapshot tests.
* Good work with testing apiCalls, actions, reducers, testing simulation changes in App, testing that methods have been called in componentDidMount, mapStateToProps, mapDispatchToProps
  * Still missing tests on methods created in App.
  * Missing many component tests with methods and changes in state in the Game component.  Would add some of those at some point since that is where a lot of the functionality lives.


## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 
* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.
* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 2 - Nearly all unit tests are in place. React components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods.  All routes have been tested as well including dynamic routes.  There are tests in place for actions, reducers, mapStateToProps, and mapDispatchToProps.  No attempt to test async functionality was made.
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.