### Evaluator: Leta
### Students: Jev, Katie, Patrick
### Comments:

* Login works but UX is clunky (route to login when trying to favorite, make it easier to create an account on a failed login)
* Functionality a little clunky (unable to unfavorite from the Favorites page, no indication of when something is favorited or unfavorited, unsure if clicks are doing anything)
* Extra features like search and genre fetches
* Responsive! Hooray!
* Redux store is pretty nested and has a lot of redundancy (refactor to store all movies in one array with genre keys, store only favorited movie IDs in Favorites array)
* Tests are a mess - mostly there but just haven't been kept up with, need to be updated to match actual application functionality
* Redux tests look pretty good

## Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.
* 2 - The application is in a usable state, but is missing part of one or more of the  features outlined above. Evaluator has multiple recommendations for design changes.

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.

### Testing

* 4 - All requirements from 3 met, all async functionality is tested, tests are passing and run efficiently (using mount only when appropriate).

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 4 - All requirements from 3 met, and always chooses the correct component for rendering, as well as the correct Route API. Application should account for undefined routes.
