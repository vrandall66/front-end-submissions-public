### Evaluator: Travis Rollins
### Students: Alek Aker & Ann Cerveny
### Comments:
* Nice work with the scrolling text
* Might make it a bit easier to see the favorite icons (greys are a little too close)
* Careful of having multiple scrolls on an app (looking at the `Alderaan` card)
  * Scroll for the window and scroll for the card can lead to a tough UX (especially on mobile)
* Missing a notification if there are no favorites
* Might continue to style the active state of a NavLink.
  * Maybe switching svg image to a different color?
* Would look into how you can create a 404 page if a user goes to a route that doesn't exist
  * `localhost:3000/yolo`
* Look into how you could break out your fetches into a separate file
* From a performance standard, likely don't need to fetch all of the data at once in `componentDidMount`
  * Only need the crawlText in the initial beginning.  You can then fetch the data needed if a user clicks on a Navigation button.
* Missing multiple catches with our fetch calls.
* Would recommend not having a favorites array.  This causes duplicate data in state.
  * Add a property to each of the objects in planets, vehicles, & people to keep track of favorites.
  * Also openingCrawl likely doesn't need to start out as an array in state.
* Might break out `fetchNested` in App into a few functions.  Gets complex quick and could be very difficult to test.
* For developer empathy, would recommend breaking out props onto separate lines (looking at render in `App`)
* Shouldn't need to pass `this.state.favorites` to "planets".  (Line 76 in App.js)
* Think about how you could refactor your Route components since they are all similar
  * Maybe using an array prototype method like you did in your `Card.js`?
  * Could also try out dynamic routing.
* `Card.js` acts much more like a container
  * Map through your data, and instead of returning a section, return a new `Card` component
* Not sure why a function exists in the map of `Card`
  * Would be easier to move it out of there instead of declaring it over and over.
  * Even more so, would recommend moving that method up to the App so that you can **test** it.
  * Love the idea of how you are using the keys.  Think about how you could use Object.keys on your props instead of just the species. (instead of having to destructure every prop, use the keys to map through and return the `p` tags you need)
* Nice work having snapshots for all 3 types of data for the `Card` component.
  * Careful of using `uuid`.  Breaks the snapshots.  It's perfectly fine to include a key like `planets1, planets2, planets3` etc.
* Good work testing simulation event for toggleFav in card.
* Would include a snapshot test `Quote` for if data.opening_crawl is undefined.
* Missing multiple tests in App
  * Would have liked to see a couple of tests for toggleFavorite and how it updates state
  * Would like a test for this `notDefined` function in Card as well
  * Would try and go back and do some async testing as well
* Good work on the README (might include pictures of wireframes as well)
  * Good number of commits, but might create a few more branches & PRs
  * Would like to see conversations on PRs and code reviews (serves as a nice paper trail)
* Good work with GH projects.  Looks like a few cards to get moved to the `Done` section.
* Nice work with not linter errors!

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

* 1 - There is little or no evidence of testing in the application.  There are some UI tests including snapshot tests, but major gaps in unit testing functionality.
* 2 - Nearly all unit tests are in place. Components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods (including `componentDidMount`).  No attempt to test async functionality was made.