### Evaluator: Robbie
### Students: Chris, Alyssa, and Aidan
### Comments:

* My lastpass asks me if I want to save my email and password for this site, so that's a good sign in terms of form design
* In a search, do you always want to clear the input of a search? Sometimes it's nice to keep the search term in the input so you can modify the search if the results are not what you expect
* The search functionality seems to be working well. It would be nice to have something say "No results" if I search for something not found
* Is the hidden search field intentional? I wouldn't mind having it shown all the time since it doesn't take up a lot of space
* The details page looks good - a good refactor would be to format the release date into something a user would expect
* On the book details page, careful with the word `back` because if I came from my favorites page, it takes me back to the main search page instead - it's not truly like a browser back button and might not be what a user expects
* Filters working well!
* Overall, features could use some polish, but they work!

* Actions and action tests look good
* For reducers, be a little more consistent with naming
* Reducers and reducer tests looked good
* Feel free to break up larger section in the App render into components
* Good try with the App router test. If this is something you're really interested in showing you can test, you're getting close!
* App component and login form testing looks good!
* Project board looks good - don't be afraid to divide up tasks a little more granularly
* Good readme - the one thing missing I was looking for is screenshots


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

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 4 - All async functionality is tested.   Asynchronous tests cover happy paths as well as multiple sad paths.  All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
