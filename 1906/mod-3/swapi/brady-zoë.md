### Evaluator: Robbie
### Students: Brady and Zoe
### Comments:

* Got a jQuery error from the get go when cloned down from master - saw that jQuery is being used in the form to clear inputs. This is a big no-no to use jQuery within a React app. Remove jQuery from the app and use state to update the form values. **Need to fix this and send back.**

* The opening form is great - nice, easy to read and fill out. No trouble there.
* Seeing all the characters and the scrolling text plus the stars moving in the background is a lot to handle visually, the red on block text is tough to read too - run your app through a contrast detector to check on levels of contrast to improve readability
* Bug: Favorites link button displays different numbers of favorites depending on what movie you view, and then going to the favorites shows favorites only for that movie - maybe this was intended, but it was not a requirement in the spec

* Why are movies being saved in localStorage?
* The `!this.state.isLoading && <Route exact path='/'` in App is kind of confusing to me. Usually, the route should always exist and shouldn't be conditional, and then the render inside that route has some conditional logic to determine what renders within that
* Nice job with the route naming conventions
* Good job with proptypes
* API calls file looks good - I like how things are broken out into separate functions - within this, `fetchCharacterData` I think could be restructured so you're not building on this `characterData` object as you go through the fetches
* Commented-out jQuery left in the CharactersContainer component...
* For the Character Card rendered in the container, use something other than the index `key={i}`, if the index for some reason changes, then it is no longer unique and ties to that card - does the character data have anything unique associated with it that could be used as a key instead?
* Why is `FavoriteCharactersContainer` a class component? It does not use lifecycle methods or utilize state.
* In the `MovieCard` component, adding the episode as a value to a button is a bit overkill for this scenario - I think passing the episode as data through the `selectMovie` is a more affective way of doing this so that you don't have to then traverse the DOM within the `selectMovie` method in `App`
* Generally, I'm not a fan of a method named `updateState` because it's very vague - what state, whose state, what about the state is being updated?

* 27 tests total
* Missing some tests for when buttons are clicked, is a function called...and if that function takes arguments, were they called with those arguments?
* I like the idea of the `'should not submit info if form is incomplete'` - walk me through this test
* I would lean toward not having `isComplete` in the form's state - instead create a function that when called can evaluate if the form is complete. This test `'should update name, quote, rank when submit button is clicked'` is a bit weird because the rest of state is empty strings, which could be a possible bug scenario in the live code
* This is a nice, simple and specific test: `'should toggle a characters favorite status for a particular movie'`


## SwapiBox Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and concise commit messages. 

### React Architecture

* 2 - PropType functionality is complete.  There are no unnecessary props being passed down to child components.  However, there are still methods that are being created inside of functional components instead of being passed down through props from a class component.  File structure is modular but api calls have not been broken out into a separate file.  
* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.

### Testing

* 2 - Nearly all unit tests are in place. Components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods (including `componentDidMount`).  No attempt to test async functionality was made.
* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.
