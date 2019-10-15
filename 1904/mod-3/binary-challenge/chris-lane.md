### Evaluator: Travis Rollins
### Students: Chris Lane
### Comments:
* Need many more commits and branches.
* Good work with README with description, setup, technologies used.  I would also recommend adding wireframes.
* Would liked to have seen a project management tool used.
* Good work, only 4 linter errors.
* Love the attempt of accessibility for being able to click the entire option (`launch`, `company`, etc.) but I still have to click the circle in order to select it.
* Don't recommend scrolling left to right.  Most users are used to scrolling up and down.
* Love that I can see some videos on the `Schedule`.  
  * Like to see the rocket types and appreciate that an image still shows if there is no available image url.
  * Companies & Missions are a bit unfinished.  Would like it to either show more, or change the layout of cards.
* Search functionality works pretty well.  How could the UX be improved?  If it doesn't find something, maybe show an error message.
  * Would be good to display some kind of error.
* Store is relatively clean for all of the data you are showing.
  * Might also include an `error` and `loading` inside of the store as well.
* Good work with actions and reducers.
* Would recommend moving components and containers into their own directories.
  * Also break out the card components into their own directories.  Since they are look similar, but display different pieces of information, look into how you can refactor these Card components into one.  Maybe use `Object.keys(props)` and map through the keys to return the data you need?
* In `App`, make sure to wrap your fetches in a try/catch so if something breaks, you can do something with that error.
  * Noticed you have try/catch in apiCalls.  Move those try catches over to the components where you call them and it should work correctly! 
* Good work including propTypes.
* Think about how some of the containers could get refactored into one like `MissionsContainer` and `CompanyContainer`.
* Remember to include unique key prop.
* Great number of tests.  Only one is silently failing in the apiCalls.
  * Great work on your actions, reducers (could get broken out into separate files), apiCalls, mapStateToProps, and mapDispatchToProps
  * Missing some tests on methods in App and what they return 
  * Could also include tests that methods have been called in componentDidMount

## Rubric 

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.
* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.
* 4 - All requirements from 3 met, and no duplication of data exists in the
  store. Data in the store remains flat (not nested).

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 4 - All async functionality is tested.   Asynchronous tests cover happy paths as well as multiple sad paths.  All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.