### Evaluator: Robbie
### Students: Victor and Chris
### Comments:

* Submission link not working...
* The form looks good - reduce the transparency more though because it's hard to read against the busy background
* Form is missing some validation (if nothing is selected in the dropdown, I can still submit)
* I like the Eject idea for signing out
* The horizontal scroll of the movies is nice, kind of a Netflix theme to it - I would add a background to the cards so they aren't totally transparent and blend into the background; the title of the movies is also tough to read because of this

* Interesting that you made your own Button component for linking - say more about this decision. Why not use a click handler for a Link component?
* Nice job with routes, they look clean and they are not redundant
* For the form, having a `formComplete: false` property can be tricky because it introduced a chance for a bug. Instead, I think making a function to evaluate if the form is complete and doing something based on the result of the function is a little safer, even if it's a millisecond slower.
* Good job with using unique information like `key={character.name}` for the keys and not the mapped array index, however there is a duplicate key warning happening in the console, so you'll have to debug that

* 24 tests written
* Missing one or two unit tests in App, but the tests that are there look good in terms of testing if state is modified
* For the `'should delete characters when removeFavCharacter is called'`, it's better to have multiple favorites in the array initially to be absolutely sure that the method is finding the correct favorite to remove
* Nice job with form testing - there are a lot of combinations to test when it comes to multi-input forms

* Some compiler warnings coming through in the terminal after `npm start`
* For your Trello board next time, be sure the columns are progression based and not feature based
* Some broken image links in your Readme - be sure to fix those if you're including this in your portfolio

## SwapiBox Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the features outlined above. There are one or more major bugs and the evaluator has multiple recommendations for design changes.

### Project Professionalism

* 3 - The codebase has less than 5 linter errors and README has been updated with all group members. Project utilized wireframes from the outset and updated them as changes were made. A project management tool was continuously used from the beginning of the project.  All git commits are atomic, made first to branches, and use descriptive and concise commit messages. 

### React Architecture

* 3 - React architecture is clean and organized.  Logic is kept out of return statements.  There are some issues with the asynchronous js where the frontend is not matching with the backend.  There are multiple functions (including fetch calls) that are doing similar pieces of functionality that could continue to be refactored. Data fetched from API is not cleaned before being set to state.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.  UX is clear and set up well so that user has access to previous routes.

### Testing

* 3 - A valid attempt to test asynchronous functionality has been made.  Asynchronous tests cover happy paths as well as multiple sad paths.
