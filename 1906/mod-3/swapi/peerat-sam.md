### Evaluator: Travis Rollins
### Students: Peerat & Sam
### Comments:
* Good start to README including collaborators and screenshots.
  * Would also like to see a description for the app, setup, and wireframes used.
  * Good work sticking with GH projects.  Would like to see iterations broken out into smaller pieces.  (what was a feature, bug, test, etc.)
* A number of linter errors.  Include this script, `"lint": "eslint src/"` in your package.json and run `npm run lint`.
* Good work on number of commits and commit messages.
  * Would like to see more branches.
  * Love the tags on PRs like `bug`, `feature`, etc.  Keep this up!
  * To take PRs to the next level, I would love to see code reviews, comments on code, etc. PRs should also have more information on them like what this commit is doing.  Come up with a template like if it fixes a bug, implements a feature.  And maybe what issue it resolves from your GH projects.
* Would highly recommend while you are loading the data, allow the user to be able to sign in. (having to wait for data they can't even see yet can cause a bad UX)
* Also a `sign out` button shouldn't be there unless the user has logged in.
* Remember to include an error if the user hasn't filled out all of the inputs on the form.
* Careful of multiple scrolls on cards for `characters`.
  * Can be a tough experience for Desktop and Mobile as the user scrolls through the characters.
* User is unable to go back after selecting a movie to check out characters.
* I don't recommend loading all of the data at once on the very beginning.
  * Fetch the data when it is needed.  (It's fine to load movies while the user is typing in the form.)
  * Then wait to load the characters for a Film until they actually click on a button.
* Remember to do something with your errors when fetching.  Set them to state and render them.
* Good work cleaning out data being fetched so that there is no extra data inside of state.
* Cheers for including propTypes.
* In state, I think it's fine to have a `user` object in state instead of all properties for name, quote, and ranking.
  * Make sure you still have state in the Form component.  Then on submit, pass it up to the App as an object.
* Think about how you can refactor the logic for the Link button.  Maybe add a condition in `submitUser` checking if all inputs are filled before it runs `udpateUser`.  
* Does the entire state object need to be passed to the `MoviesContainer` component?
* Quite a bit of extra data included in the `Route` for displaying the characters.
  * I love that you are using the id from the params, but instead of doing multiple finds to return specific properties, pass the entire object through.
  * Also, why do you need to pass the entire state to `CharacterContainer` if you just found which movie data you need?  Pass only props that you need.
* How can you reactor the `MoviesContainer` and `CharactersContainer` into one component?
* Would like to see many more tests for all of your components.
  * Missing tests for `CharactersCard`, `MoviesCard`, `UserInfo`
  * Some good tests with the `App` component.
  * Good work mocking out `getFilms` and checking that it's called after mounting.
  * Some great event simulation tests and testing changes in state.
  * Good start with testing isolated fetch calls.  Make sure to test sad paths as well.  ( also double check some of the warnings you are getting on your tests.  `Cannot read property map of undefined`)
    * Look at what your Promise is resolving for `getFilms`.  Then look at what your implementation is doing.  The promise you mocked is resolving an array, but in your implementation it is an object with a property of results (which then has the array).


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

### Testing

* 2 - Nearly all unit tests are in place. Components are well tested with a diverse set of tests including but not limited to snapshot tests, event simulation tests, and tests on class methods (including `componentDidMount`).  No attempt to test async functionality was made.
* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.