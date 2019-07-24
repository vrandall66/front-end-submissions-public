### Evaluator: Travis Rollins
### Students: Evan Markowitz & Andreea Hanson & Jacqueline Moore
### Comments:
* Remember to include a 404 error page if route doesn't match
* In the app, see about spreading the properties through instead of having to write each one out
* Remember to include await before an asynchronous function
* Double check to make sure all containers are included in the containers directory
* Awesome work including cleaner functionality for the movies
* There is a little duplicated data in the store.
  * Would recommend keeping track of the movie_id as opposed to storing the entire object in the array.
* Consider the way you name properties so you don't have to rename when making posts/deletes/etc.
* Finding ways to break out conditionals and how to utilize props from you store so you don't have to repeat that in component state
* Remember to include props from store (mapStateToProps, mapDispatchToProps) into your propTypes
* Network requests can be costly.  Would recommend adding favorites through the store as opposed to fetching your favorites again.
* Great work on your README and number of commits.
  * Continue to work on consistency with conversations on PRs and PR reviews.  


## Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

  [10 Essential Usability Guidelines.](https://speckyboy.com/10-essential-web-application-usability-guidelines/)

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.

### Testing

* 4 - All requirements from 3 met, all async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).
* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.
* 2 - At least one component is not connected with Redux appropriately. Application state is mutated by more than just Redux. The Redux store is missing application data that it should be handling.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
