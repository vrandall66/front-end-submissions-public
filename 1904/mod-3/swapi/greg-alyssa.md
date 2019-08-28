### Evaluator: Travis Rollins
### Students: Greg & Alyssa
### Comments:
* Could have more clarity for what is interactive with the favorite button
* Would be nice to have some kind of labels for each data point on a card (1 of what?)
* Styling could use more work
  - Text is a bit small & difficult to read
  - Would spend a little more time on the scrolling text
  - Dark theme is awesome, but the contrast with yellow pops out a bit too much (Maybe check with an accessbility tracker?)
* Nice work with the dynamic routing!  (good extension)
* From a performance standard, don't fetch all of the data all at once
  - Fetch when a user clicks on "planets", "vehicles", etc.
* Careful on chaining `.then` for each fetch
  * If any one of those fetches fails, it will break the entire app
* Might break out cleaning functions into a helper file
* Duplicate data in state.  Favoriting the entire card inside another array
  * No need for favorites array in state.  Add a property in all of your people, vehicles, planets to keep track of favorite.  
  * No need for `isFavorite` as well in state. (keep state a minimum)
* Routes & NavLinks could get refactored
  * Either using an array prototype method or making routes more dynamic
  * Look into how you can create a `404` page if I go to something like `localhost:3000/yolo
* `Card` acts more like a container as opposed to a Card
* Instead of destructuring every single possible prop in your `Card`, use something like object.keys to get all of the keys from your props.
* Good work with snapshot tests and route notes
  * Remember to include tests for dynamic routes
  * Missing route test for `favorites`
* Would like more tests for class methods
  * In the `Card` test include multiple snapshots for all types of data.  
  * I recognized many of the other methods in `App` were async, but there could have been a test for `identifyVehicleInfo` to make sure it returns the output you expect.
* Good work with testing `addFavorite` function in App.test.js and simulating event for `addFavorite` in Card.test.js
* Good start trying to break out fetch calls.  I might try breaking one out, and then implement it back in the component to see if it works!
* Good consistency with commits and decent amount of branches 
* Leave a paper trail with your PRs
  * Leave comments on each other's code, things to update etc.
* Good work sticking with GH projects
  * Might break this out into more columns, like `Upcoming`, `In Progress`, `Finished`, etc.
* Would recommend leaving labels for screenshots on README


## SwapiBox Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.

### Testing

* 2 - Nearly all unit tests are in place. Components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods (including `componentDidMount`).  No attempt to test async functionality was made.
* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.