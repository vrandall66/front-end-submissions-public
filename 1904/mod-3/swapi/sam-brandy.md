### Evaluator: Robbie
### Students: Sam and Brandy
### Comments:

* I like the background, there is a lot of depth there
* If I don't have any favorites, go to the favorites page and then refresh, then I see the scrolling text...
* If there are no residents for a planet, then give some default value/text to be displayed
* I like the green highlighted border if a card is a favorite, it's a nice balance of subtlety
* There is some kind of footer that is blocking the cards from being seen at the bottom of the page

* Any reason the Favorites nav link is a separate component and outside of the other nav links container?
* Why the need for the `section` wrapper element here? https://github.com/SamanthaLFreeman/GalaxyFarFarAway/blob/master/src/components/FavR2D2/FavR2D2.js#L9
* An empty `alt` attribute?? https://github.com/SamanthaLFreeman/GalaxyFarFarAway/blob/master/src/components/FavR2D2/FavR2D2.js#L11
* This API call is good - I think it could use a refactor around the `forEach` for getting the planet residents into the planet info: https://github.com/SamanthaLFreeman/GalaxyFarFarAway/blob/master/src/Fetch/Api/api-calls.js#L58-L77
* Careful around having an `isFavorite` property and a favorites array. This is essentially storing the same data in two different places, which gives rise to potential discrepancies between what is favorited and the favorites array.
* Overall, nice, clean render in the App. Consider a refactor of the routes to be iterable - the component is the same, but the difference is the data passed in: https://github.com/SamanthaLFreeman/GalaxyFarFarAway/blob/master/src/components/App/App.js#L87-L90
* How might you refactor all of these props? https://github.com/SamanthaLFreeman/GalaxyFarFarAway/blob/master/src/components/CardContainer/CardContainer.js#L10-L24
* A nice touch: https://github.com/SamanthaLFreeman/GalaxyFarFarAway/blob/master/src/components/CardContainer/CardContainer.js#L29
* Consider using a `nav` element here instead of a `section` https://github.com/SamanthaLFreeman/GalaxyFarFarAway/blob/master/src/components/Categories/Categories.js#L9

* Great job getting those fetch call tests in there
* Overall, good state update test for updating the favorites. What about testing `toggleFavorite`?
* What if there is no data passed in? https://github.com/SamanthaLFreeman/GalaxyFarFarAway/blob/master/src/components/CardContainer/CardContainer.test.js


## SwapiBox Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 4 - Codebase has zero linter errors/warnings and README is well documented with images of different pages, setup, purpose of application, and group members. Project team uses a rebase workflow, taking advantage of github issues to track work.

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.
* 4 - Functions including fetch calls have been refactored to be reusuable for multiple queries.  Frontend data always matches the backend data.  Data fetched from API is run through a cleaning function (which lives in a separate file).  Implements excellent error handling if server is down or fetch fails.  This includes loading images as well as error messages on the frontend.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.

### Testing

* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.
* 4 - All async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).  Unit tests for snapshots and methods cover not only happy paths but also sad paths.  Evaluator has no recommendations for testing.