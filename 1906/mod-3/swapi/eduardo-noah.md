### Evaluator: Travis Rollins
### Students: Eduardo & Noah
### Comments:
* Great work with README including description, setup, collaborators, screenshots, AND TRELLOBOARD!  (cheers!)
  * I would also recommend including wireframes in your README as well.
* Great number of commits and keeping the descriptive.
* Also cheers to adding some GH issues.
* Nice work sticking with your Trello board.
  * I might continue to breakout those tickets to even smaller pieces rather than iterations.  That way each PR resolves a ticket.
  * Would love to see code reviews and PR template for each PR.
    * What issue is the PR resolving?  Is it a feature, a bug fix, or a test?
    * Make sure to pull it down, give feedback, leave a code review.  (even if you worked on it together)
* Double check linting errors.  If you are going to use `airbnb`, they have very strict linting rules.
  * If you just want to use the linters included in react, add the script `"lint": "eslint src/" ` in your package.json and run `npm run lint`.
* Nice extension for the color coding/ranking based on being a `jedi/sith`.  
  * Also a cool feature that the button to submit only shows up if a user fills all of inputs.  Might be something to check on accessibility though.
  * Note that you don't need to use an `id` for the styling of elements.  Keep ids unique and classes for styling.
* Pay attention to class names.  Something like `character-h2` isn't the best.  Try targeting it by doing something like `".character-card h2"`.
* Some issues with sticky nav bar with scrolling (gets stuck in certain places)
* Remember to have a button to take the user back to movies on the `favorites` and `characters` route.
* Look into how you could create a 404 page if the route doesn't exist.  (say if I go to `/yolo`)
* Some text gets cut off on `characters` route like the Title.
* Note that logging out doesn't actually clear out the user.  (I can relog back in without having to fill anything out.)
* Long time to wait for movies to fetch and display anything.
  * Maybe fetch only movie data. 
  * Then fetch a specific movies' characters if the user clicks on a movie.
* Reminder to include a `catch` on fetches and do something with the error (set it to state and render it)
* Good work filtering data you only need and setting it to state.
* Great work with the functionality of favoriting.
  * I would recommend including a class to show that certain characters have been favorited.
* Likely don't need `favoriteCharacters` in state.  Maybe was leftover from before?
* Stay away from having to travel the DOM and updating it as in your `favoriteNewCharacter` method.  See how you can do so with React.
* Relying on `reduce` a bit too much.  Many situations where you can use `map` like in `favoriteNewCharacter` or `filter` in `FavoritesContainer`.
* How could `FavoritesContainer`, `MoviesContainer`, and `CharacterContainer` be refactored into one?
* Careful of including logic inside of return state like in `MoviesContainer`.
* Don't forget to include PropTypes!
* Good start to tests.
  * Try writing some apiCall tests this next week!
  * Good work writing some tests for the App component including snapshots, event simulations, and changes in state.
    * For the last two tests, likely not the most helpful executing a method and then checking if it has been called.
    * Rather, in something like `componentDidMount` (which fires when you `shallow` render the component), check that methods like `apiCalls` has been fired.
  * For some snapshot tests where you are using `Date.now`, look how you can mock this out so it returns the same number every time.  (there is an example of this in the unit testing lesson)
  * Good start with the `splash test`, remember to simulate some events for checking to see that `handleOrderColor` or `setRank` is also called.
    * Could be good to have another snapshot test for the conditional rendering part of this component as well.

## SwapiBox Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.
* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and consise commit messages. 

### React Architecture

* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  
* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Routing

* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.
* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.

### Testing

* 1 - There is little or no evidence of testing in the application.  There are some UI tests including snapshot tests, but major gaps in unit testing functionality.
* 2 - Nearly all unit tests are in place. Components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods (including `componentDidMount`).  No attempt to test async functionality was made.