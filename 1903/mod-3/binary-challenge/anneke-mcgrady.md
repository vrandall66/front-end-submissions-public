### Evaluator: Travis Rollins
### Students: Anneke McGrady
### Comments:
* Good consistency with commit messages, could continue to break out some of the bigger commits into smaller ones
* Cheers to using a GH project to track your progress
* Could spend more time on CSS, and make it responsive
* Should be able to click on entire tab instead of just `See More`
* A lot of data being fetched at the beginning on componentDidMount (would recommend breaking them out into their own cleaner files)
  * Would recommend fetching only when a user has clicked on a specific tab
  * Then save that data in the store & only fetch if that data is in the store
* Would recommend on line 186 in your App.js, that you have some kind of logic if the article is not found.  Maybe go to your NotFound page?  
  - Example if I hit `http://localhost:3000/health/po-1000`
* Good work showing an error, would recommend making it easier to see instead of small text at the top.
* Nice work on the 404 page!
  * Also good routing with back buttons etc.
* ADD_GIF shouldn't be firing multiple times.  Should only need to fire adding the gif once.
* In the App test, for mapStateToProps, would recommend adding more properties to your mockState to make sure you are getting the exact properties you expect.
* Missing some tests for ADD_GIF in actions, mapStateToProps, mapDispatchToProps
* Good work with propTypes


## Rubric

### Specification Adherence

* 3 - The application uses the above technologies to a professional level. The evaluator has minimal recommendations for refactoring or design changes.

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 4 - All requirements from 3 met, and always chooses the correct component for rendering, as well as the correct Route API. Application should account for undefined routes.
* 3 - Application uses React Router to display appropriate components based on URL.
