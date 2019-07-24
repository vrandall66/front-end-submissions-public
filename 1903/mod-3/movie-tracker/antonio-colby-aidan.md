### Evaluator: Travis Rollins
### Students: Antonio Fry & Colby Allen & Aidan McKay
### Comments:
* Login functionality is solid, a couple bugs with favoriting.
  - Unable to addFavorites/removeFavorites after creating account.
* For UX, it would be awesome to have a way to go back to home page
* Continue to work on conditional rendering.  If I haven't signed in yet, I should be able to add/delete favorites.
* Would look into creating a 404 page if page doesn't exist.
* Cheers to using propTypes
* Might refactor some of the NavLink so it's not quite so lengthy including the signout functionality (make it it's own component)
* Make sure containers are inside a container directory.
* Continue to work on refactoring signup and login components.
* Good work with error handling
* Continue to be consistent with either using async/await or .then
* Would recommend a cleaner functionality for cleaning out unneeded data from the movies
* Should only need to keep track of movie_id instead of entire object for favorites
* Solid effort towards testing especially with actions, reducers, containers, etc.  
  * Some good work with testing components as well.  
* Remember to utilize something like a TrelloBoard. 
  * Also make sure to leaves comments on code for PRs.

  
## Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the  features outlined above. Evaluator has multiple recommendations for design changes.

  [10 Essential Usability Guidelines.](https://speckyboy.com/10-essential-web-application-usability-guidelines/)

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.
* 2 - Project is missing PropTypes, README updates, wireframes, or has more than 5 linter errors. Project team makes large infrequent git commits. Project shows a basic understanding of React.

### Testing

* 4 - All requirements from 3 met, all async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
