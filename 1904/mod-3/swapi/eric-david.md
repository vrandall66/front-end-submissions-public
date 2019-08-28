### Evaluator: Robbie
### Students: Eric and David
### Comments:

* Clickable area for the favorite lightsaber is pretty small (more so that the dark lightsaber makes it hard to see where to click) - would probably be tough on mobile, possibly make the favorite word clickable as well
* I like the inverse coloring when something is favorited
* For "extra" cards at the bottom, would like to see you try to stack them in line with the other cards from left to right
* The nav icons are great, and the favorites counter in the nav is nice too

* Great job separating the fetch calls and data-cleaner functions in the `util` file
* Nice, clean App render - I like that you extracted the Header to its own component
* Use a more descriptive variable name for your `data` here: https://github.com/davidagitlen/SWAPIbox/blob/master/src/Header/Header.js#L11
* `nav` would probably be a more semantic/descriptive HTML element here instead of a `div`: https://github.com/davidagitlen/SWAPIbox/blob/master/src/Header/Header.js#L17
* Nice job using propTypes throughout your components
* Good job having some content if there are no favorites yet selected
* Consider a refactor here where since each of these data points is in a `p` tag, could you make this information iterable instead of hard-coding all of the possible `p` tags? https://github.com/davidagitlen/SWAPIbox/blob/master/src/Card/Card.js#L44-L54
* Tell me more about why these attributes are necessary: https://github.com/davidagitlen/SWAPIbox/blob/master/src/Card/Card.js#L37-L38
* I'm very torn on the mixing of local storage and setting state in this method, I think mainly because the method is called `addToLocalStorage`, but it also manipulates state: https://github.com/davidagitlen/SWAPIbox/blob/master/src/App/App.js#L64-L67 So it's not apparent at first how the state gets modified in the `favoriteCard` mainly because of the method name.
* Even consider a refactor of the `Route`s to make this section iterable: https://github.com/davidagitlen/SWAPIbox/blob/master/src/App/App.js#L80-L86 The component is the same, but only the data is different.

* Get rid of this test: https://github.com/davidagitlen/SWAPIbox/blob/master/src/App/App.test.js#L15-L17
* Good job testing the various snapshots of the same card: https://github.com/davidagitlen/SWAPIbox/blob/master/src/Cards/Cards.test.js#L43-L57
* Nice work getting a couple fetch calls tested in the `util` file
* I'm curious why you need this line in your test: https://github.com/davidagitlen/SWAPIbox/blob/master/src/App/App.test.js#L24 Is setting a favorite affected by what is in the people array?


## SwapiBox Rubric

### Specification Adherence

* 4 - The application completes all iterations above and implements one or more of the extensions.  The evaluator has no recommendations for design changes.

### Project Professionalism

* 4 - Codebase has zero linter errors/warnings and README is well documented with images of different pages, setup, purpose of application, and group members. Project team uses a rebase workflow, taking advantage of github issues to track work.

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.
* 4 - Functions including fetch calls have been refactored to be reusable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.

### Testing

* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.
* 4 - All async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).  Unit tests for snapshots and methods cover not only happy paths but also sad paths.  Evaluator has no recommendations for testing.