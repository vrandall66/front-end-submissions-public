### Evaluator: Travis Rollins
### Students: Jacob Ogren & Djavan Munroe
### Comments:
* Love the scrolling text on the root page
* Great implementation of localStorage to persist data
* Fun hover effects and active state for buttons
  * Also love the LightSide & Darkside effect! Nice creativity!
* Would like to see a 404 page if I go to something like `localhost:3000/yolo`
* Would like to see a loading icon so I don't think the app is frozen.
* Nice accessibility to all routes
  * Might look into how you can make all Links available without having to hover
  * Never would have guessed the title or Darkside effect existed (for accessibility)
  * Dynamic routing for each character could also have a better visual cue (had no idea I could click on a card until I looked at the code)
* Would recommend not fetching all of the data right at the beginning.  Fetch the opening_crawl since that will be on the root.
  * Then fetch the data necessary when they click something like `Planets`.  Will help with performance
* Not a fan of console.logs for errors.  Show us the error on the UI.
* Nice work breaking out the functionality for favoriting.  
  * Would recommend not adding the entire object into the favorites array.  This creates unnecessary duplicate data.  Add a property of favorite to your data (`planets`, `vehicles`, etc.) and then update as necessary.
* If a ternary is longer than a line, break it out into an if/else.  (Line 27 in App)
* Good work with routing, might look into how you can refactor it
  * Map through it returning each Route component, or try dynamic routing for planets, people, vehicles
* Would break out props onto separate lines for developer empathy (looking at render in App)
* Could have some overall refactoring with `Card` component
  * Instead of destructuring all possible props and writing out all of the `p` tags, how could we use something like `Object.keys` to get the keys of the props? Then map through the keys to return the `p` tags necessary.
* Good work breaking out apiCalls into a separate file 🎉
* Solid work on your tests
  * Good work with the testing for `toggleFavorite`.  I would like to see tests for addFavorite & removeFavorite and even toggleTheme as well
  * Nice work with tests for routes and dynamic routes
  * Nice work with snapshot tests for all types of data on the `Card` as well as doing a simulation test to make sure toggleFav has been called
  * Remember to include a test for `Landing` as well
  * Nice start to testing your apiCalls 
* Good work with README (would recommend labels for each of the images)
* Not happy that there is only a `master` branch and no PRs.
  * Not good GH workflow, and not a papertrail for future employers.
  * Want to see branches and PRs (along with conversations on those PRs and code reviews)
* Good work sticking with GH projects
* Good work with linter

## SwapiBox Rubric

### Specification Adherence

* 4 - The application completes all iterations above and implements one or more of the extensions.  The evaluator has no recommendations for design changes.

### Project Professionalism

* 1 - Either the README is incomplete, wireframes are not used, no project managment system was utilized, or more than 10 linter errors are present. Git history does not show evolution of project with many large and inconsistent commits. 
* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.

### Testing

* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.
* 4 - All async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).  Unit tests for snapshots and methods cover not only happy paths but also sad paths.  Evaluator has no recommendations for testing.