### Evaluator: Travis Rollins
### Students: Jeannie & Pol
### Comments:
* Good work with README including description, setup, and screenshots.
  * Remember to include contributors and wireframe pictures as well.
  * Good work sticking with GH Projects.  Would like to see you break iterations into even smaller piecess.  Would be awesome to have a card for each time you fix a bug or add a feature, or test something.
* Good work including GH issues as well
* Great number of commits and staying consistent with commit messages
  * Not good only having one branch. Make sure to create a new branch each time!
  * Also the fact that there are no PRs is also not great.  Make sure to have PRs before each commit.  Would like to see code reviews between each other.
* Good work only having one linter error!  Cheers!  (you can include this script, `"lint": "eslint src/"`, in your package.json and run `npm run lint` in your terminal)
* Great error handling on the form.
* Make sure the background covers the entire screen
  * Good work with loading icons 
* Might include the crawl above so the user can see it.  Good work showing the data though.
* Would be nice to have a button that routes me back to the movies section.
* Look into how you can create a 404 page if a route doesn't exist `/yolo`
* Appreciate having a user object inside of state.  This is great!
* Remember to include a `catch` on fetches so you can handle it if it errors out and render it.
  * When getCharacter info with your fetch, something to think about is whether you need to fetch ALL of the characters.  Currently we are only displaying the first 10, so it might be a better performance boost if the user only fetches data necessary.
* I would recommend breaking out props onto separate lines in renders for readability reasons.
* Good work breaking out apiCalls into their own functions.  Makes them much easier to test in the future.
* It's interesting the default ranking is `"Space Balls"` but the option is "Padawan".  Could be confusing for a user.
* Would like to see more tests in the future.
  * Good start with the App test.  Continue to test other methods like `selectMovie`, `componentDidMount`, `setCurrentCharacters`
  * Excellent testing with snapshots, changes in state, and event simulations in the `Form` component.  Also good tests in `MovieCard` testing that the button was clicked.
  * Double check your snapshot test for `characterCard`.  Notice it is trying to map through films.  Make sure you are passing an array as a prop for `films`.
  * Try and do some async testing in the next week or so!
* Completely missing propTypes.  Remember to include those for your components.


## SwapiBox Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.

### Project Professionalism

* 2 -  README has been updated but is missing group members, setup, tech used, application images, or etc.  Wireframes are included and a project management tool was started, but are not utilized throughout the entire project. Project has more than 5 linter errors. Project team makes large infrequent git commits. 
* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  
* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Routing

* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.
* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.

### Testing

* 2 - Nearly all unit tests are in place. Components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods (including `componentDidMount`).  No attempt to test async functionality was made.