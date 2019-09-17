### Evaluator: Robbie
### Students: Brandy, David, and Brianna
### Comments:

* Nice landing page displaying the different genres
* The overall page is pretty bright for me, but I think that is somewhat personal preference - it's a pleasant use of a gradient for once on the web!
* I like that if you try to favorite something, it prompts you to sign in
* In a search, do you always want to clear the input of a search? Sometimes it's nice to keep the search term in the input so you can modify the search if the results are not what you expect
* The search functionality seems to be working well. It would be nice to have something say "No results" if I search for something not found
* Possibly hide the create account form by default since it is less frequently used and takes up a bit of real estate on the top of the page
* My lastpass asks me if I want to save my email and password for this site, so that's a good sign in terms of form design
* The top section of the main page ("Welcome Alan!") is so big and only displays text - think about how to rearrange this information to utilize the page space
* "My Collection" with nothing in it displays an empty narrow bar - consider some indication that there is nothing in the collection yet or else a user will think something might be wrong

* Not seeing dynamic routing being used for the book details page - this still feels very much like a single-page application since the collection is also on the home page filling in the top section.

* 88 tests at time of eval, a lot of tests! 2 tests hard failing, can't see the whole output to verify all tests.
* Actions and action tests look good
* Reducers and reducer tests look good
* Looks like you attempted router testing - what did you end up trying?
* Tell me more about decision to store all books in state instead of redux (not saying that this is bad)
* Lots of async tests written, which is great to see



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

* 2 - Application uses React Router, but does not display the appropriate components upon navigating.  There are one or more issues with the UX and access to routes is either unclear or not full implemented on some pages.
