### Evaluator: Leta
### Students: Hindreen, De'Marcus, Ryan
### Comments:

* Redux store is a bit nested (favorites is an array with a single array of favorited movie objects in it, userDetails does not need to be in its own object)
* Info in Redux store is redundant (favorites should store IDs not the whole movie object)
* UX: buggy - can't unfavorite, no indication that something was favorited, can favorite multiple times, login doesn't prompt sign up, doesn't reroute to logged in homepage after signing up
* UX mostly working now, but Redux store is still nested - when in the favorites view, no obvious way to get back to home page, clicking "Movie Tracker" logs you out! WEIRD!
* Tests are breaking - seem like updates to codebase were made without updating test suites
* Tests fixed


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
