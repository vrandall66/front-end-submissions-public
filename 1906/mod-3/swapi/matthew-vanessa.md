### Evaluator: Travis Rollins
### Students: Matthew & Vanessa
### Comments:
* Excellent work with README including languages it was built with, description on how app works, link to deployed app, and link to project management board.  Cheers!
  * Remember to include screenshots of your app and wireframes!
* Solid work on commits and commit messages.
  * Make sure to stay consistent with how you are [naming branches](https://github.com/vrandall66/SWAPI-Trivia/branches/active)
  * Would like to see more of a PR template for each PR including whether it was a bug fix, feature, test, and what ticket it is resolving.  Would also love to see code reviews on PRs (even if you worked on it together).
* Think about how you can continue to break out your tickets on your Project board.
  * What tests are you wanting to implement?  What routes are still missing?  It would be great to have a ticket for each PR.
* About 5 linter errors.  To double check, include this script in your package.json: `"lint": "eslint src/"` and then run `npm run lint` in your terminal.
* Interesting to see the Profile part on the login section.  Potentially it might be better to use conditional rendering and only show it after they have logged in.
  * Love the UI of the Profile though.  Cool idea with the lightsabers.
* Some cool ideas with how you have implemented modals.  Clicking on a movie brings up a modal that shows more information.  Very cool.
  * The lightsaber x button to close out of the modal could be a bit bigger to make it easier to get out.  Or maybe the modal doesn't cover the entire screen, and so if a user clicks outside of the box, it closes as well.
* I love that the crawl for the movie appears while the user is waiting for the characters to show up.
* I might change the color of the character cards as it can be a bit difficult to read with the black background as well.
* Maybe favorite button could be a bit bigger or hoverable?
* It would be great to have a `Back` button on the characters page so the user can go back to see movies.
  * The user can go to `Favorites`, and then see movies which is great.  
* Look into how you can create a 404 page if a user goes to a wrong route `/yolo`
* Don't need catches in `apiCalls` as long as you have the `catch` in the component.
  * Remember to do something with the error.  Set it to state, and render it.
  * Also remember to have a check on the response before return `response.json()` checking if the property is ok.
* Overall I like how the apiCalls are broken out out into smaller functions.  Makes it much easier to test.
* I would recommend running some kind of cleaner function on movies before you set it to state.  There is a lot of extra data there that you don't need.
* I like that you are using another `componentDidMount` for the `charactersContainer` and only fetching the data needed.  (instead of fetching all characters from the very beginning).
  * If we changed some of the architecture, could it be possible to combine the `charactersContainer` and `favorites` into one component?
* Interesting to see you using the `react-modal` package.  Good research, it is a great package!
* Noticing you have to `/` root routes.  Only need to have one. (on lines 113 and 128 in `App`)
* In `handleSubmit` with your `Form` component, do not need to use `history.push`.  Try using a `Link` component instead that wrapers the submit button.
* I might sort the movies as soon as you set it to state (so it doesn't have to sort repeatedly every time the `MoviesContainer` renders.)
  * `createMovieObjects` is a nice cleaning function.  I would move that up into a class component so you can test it.
* Don't forget about your PropTypes!
* Great work on the number of tests
  * A couple snapshot tests that need to be updated.
  * Excellent work testing your methods inside of your `App` component.  Try and test your `componentDidMount` as well!
  * Some good simulation tests in your `UserProfile` component.
  * Great work on the isolated fetch tests.  One thing I noticed was with the sad path test, you are using `Promise.reject` and passing in an object with ok set to false.  In order to hit that conditional, make sure it is `Promise.resolve`.  Then have another sad path test for `Promise.reject`.


## SwapiBox Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

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

* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.
* 4 - All async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).  Unit tests for snapshots and methods cover not only happy paths but also sad paths.  Evaluator has no recommendations for testing.