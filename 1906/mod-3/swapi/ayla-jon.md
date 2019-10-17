### Evaluator: Travis Rollins
### Students: Ayla & Jon
### Comments:
* Would like to see more info on your README.
  * I appreciate description and technologies used, but would also like to see links for each collaborator(take them to your GH profile page), screenshots, wireframes,trello board used, etc.
    * I noticed you closed the Trello board, but think it's useful to open it up (not only for the eval but also for other people to see your workflow).
* Excellent number of commits.
  * I think some commit messages could be a bit more descriptive like [More form testing](https://github.com/ayladharamsey/trivia/commit/76d3d2f048f74e309278175f08801fe8e274e123) and [updates, data manpiulation, etc.](https://github.com/ayladharamsey/trivia/commit/71658d36d217f6a9e69f17b84075cdb8c9b7698c).  
* Would also like to see more information on PRs.
  * Use some kind of PR template.  Does this add a new feature, fix a bug, add a test. Does this pertain to a specific ticket on your Trello board?  etc.
  * It would also be great to some code reviews/conversations on each PR.  Pull it down, test it, leave feedback.  Even if you wrote it together, it provides a nice paper trail for future employers.
* Quite a number of linter warnings.  Thankfully, React already has one installed.  Add the script `"lint": "eslint src/"` into your package.json and run `npm run lint` inside of your terminal to see them.
* Should not be using jQuery in a React application.
  * Also should not need to be installing a history package.  React Router already handles history for you.
* As a user when first logging in, it would be nice to have some kind of error showing if the user didn't fill out all inputs.
  * Disabled functionality works, but if you do this, it could be helpful to have some styling differences for when it is/isn't disabled.
  * Able to login without selecting a `Jedi Rating`.  
* Favorite route breaks if I try to click on it.
* Cool work with being able to click on a movie, show the crawl, and then be able to check character info.
  * Potentially the text of `characters` on each movie card on the button might be misleading since it leads to the opening crawl first.
  * I might make the `Go to Characters` a bit more visible (ie bigger) on the opening crawl page so it's a bit easier to see.
  * `Stop Audio` would also be nice to be on the top so it is easy to pinpoint.
* Notice that characters are not dynamic just yet.  (characters are the same for each movie).
* A few styling issues with text rolling off cards for each Character.
* I appreciate the hover for favoriting characters, but it could also be nice to see that active state after favoriting a character.  
* Could be nice to have a `Back` button both on the crawl and character cards, so that I can go back to see my movies (as opposed to having to log out).
* Cheers to including PropTypes!
  * Make sure your propTypes are matching what you expect.  Got quite a few warnings in the console.
* Interesting to see that you have planets inside of state and `setPlanets` function but they aren't being used.
* Good work separating the fetches into their own file.
  * I would recommend not fetching all of the data right at the very beginning.
  * Fetch what is necessary (movie data).  Then if a user clicks on character info, fetch then.  This breaks up the network requests so there isn't as much to load.
* Make sure you have catches for all async functions in your `componentDidMount`.  There is one for `movieTitles` but not for `getMovieCharacters`.
  * Make sure to do something with the error.  Set it to state, render it!
  * Some of the chaining I think could get refactored as well like `getMovieCharacters`.  You can run multiple functions inside of a then.
* Don't need a favorites route for every `movie_id`.  There can be a route for favorites that is for all of the characters from each movie.
* How could we combine components like `MovieCard` and `CharacterCard` into one component.
* Container quite a bit of conditional logic.  How could it be refactored?
  * If the data is cleaned (removed properties that aren't necessary), pass the props that are needed.  Then on the Card component, maybe run something like `Object.keys`.  For each prop, iterate through and return a `li` tag for each property.
* Good start with tests, just a few failing. (double check errors, mostly syntax issues)`
  * Some excellent tests in Form.  Likely don't need a test for default state (since this is essentially testing the constructor).
    * Good tests on changes in state with Form and simulation events.
  * Note in the apiCalls.test.js, you do not need the `async/await` here.
  * The test for your `movieTitles` where the property of ok is set to false is written well.  The reason it is failing is because there is no conditional logic in the implmentation before you `json` the response.
  * I would like to see more async tests in the future.  Testing async methods like in your `componentDidMount`.  

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