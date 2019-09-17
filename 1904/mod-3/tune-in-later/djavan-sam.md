### Evaluator: Robbie
### Students: Djavan and Sam
### Comments:

* Really like the aesthetic of the home page - it's very clean
* The Favorites button has some room to grow stylistically, but it does at least match
* The display of each book on the homepage is great - super clear and easy to see what everything is
* The search functionality seems to be working well. It would be nice to have something say "No results" if I search for something not found
* In a search, do you always want to clear the input of a search? Sometimes it's nice to keep the search term in the input so you can modify the search if the results are not what you expect
* My lastpass asks me if I want to save my email and password for this site, so that's a good sign in terms of form design
* The genre filtering is great - would like to see which filter is active
* The book details page is nice - narrow the width of the page to reduce line length, and it would be nice to still see the image of the book
* On the book details page, careful with the word `back` because if I came from my favorites page, it takes me back to the main search page instead - it's not truly like a browser back button and might not be what a user expects
* Features are all there and not buggy - great work!
* Still signed in after refresh!
* Is the favorited button like a bookmark?

* Files are all modular, organized, and named well
* Overall I like the structure of your redux store - it's pretty flat and there isn't much duplicated data - tell me more about why you want to store the favorites in the store
* Actions and action tests look good!
* Be sure to be consistent with semicolons (in actions index file)
* Reducer and reducer tests look good!
* Good job mocking your props in the App test (in place of Redux handing down the props)
* I would move the `releaseSplit` business into a helper function
* `it('should', ()` for Book snapshot test...
* Since your mock state is repeated a lot in test files, how could you DRY this up?
* No linting errors/warnings - nice
* Solid API calls testing - what was a challenge there?
* In App, be consistent about order of params in `postFavorite` and `deleteFavorite`
* In App, could the logic for this route be moved somewhere else? `<Route path='/book/:id' render={({ match }) => {...`
* In book, definitely a refactor opportunity for the `shortName` process
* Project board looks good


## Rubric 

### Specification Adherence

* 4 - The application completes all iterations above and implements one or more of the extensions.  The evaluator has no recommendations for design changes.

### Project Professionalism

* 4 - Codebase has zero linter errors/warnings and README is well documented with images of different pages, setup, purpose of application, and group members. Project team uses a rebase workflow, taking advantage of GitHub issues to track work.

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous JS where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.
* 4 - All async functionality is tested.   Asynchronous tests cover happy paths as well as multiple sad paths.  All pieces of functionality have been tested and are passing and run efficiently (using mount only when appropriate). Evaluator has no recommendations for testing.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.
