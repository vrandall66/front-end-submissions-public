### Evaluator: Robbie
### Students: Brianna
### Comments:

* Good job on the nested routing - almost counterintuitively, `http://localhost:3000/candidate/P80001571/committee/C00580100` should be using plurals: `http://localhost:3000/candidates/P80001571/committees/C00580100`, but you will learn more about this in mod 4
* For dynamic routing, nice job passing in the `match` information instead of handling that in the Route component
* `Sarandon, Susan: $ 2,800 (2020)` for Bernie 2020, which makes me think it would be interesting to search by contributor, but that would be quite the nested lookup...
* While selecting a committee, it would be nice to see some kind of placeholder on the right window so it isn't blank
* Great that you got SASS hooked up and going
* Is `candidate` needed as a prop for the `App` container - I'm just not seeing the connection
* 93 tests! Any you have questions about?
* I would remove the root reducer test (`expect(true).toEqual(true)`)
* Brianna seeing a behavior where going to a route directly does not pass pass information through the `match`, and therefore could not use that information to fetch data for that page, how to handle this if not coming in from `Link` or `NavLink`

## Rubric 

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and concise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous JS where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 4 - All async functionality is tested. Asynchronous tests cover happy paths as well as multiple sad paths. All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing.

### Routing

* 4 - React Router components have been refactored for developer empathy and code quality is clean.  Application accounts for undefined routes. UX is excellent and set up well to have links to all routes on all pages.