# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/meloncatty/palette-picker)

#### Link to the Deployed Application
[heroku](https://kh-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/meloncatty/palette-picker/tree/iteration-002)  
This branch became 'unmergable' after I accidentally reinstalled knex.
Tests are not working, though they are annotated anyway.

## Completion

#### Were you able to complete the base functionality?

No. I did not have enough front-end functionality completed by the time I started working on implementing endpoints. Not able to parse error coming back from DELETE, so that is not implemented.

#### Which extensions, if any, did you complete?

None.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/meloncatty/palette-picker/blob/c281405c3b4f70663e5f3b5acff53c17cc430d25/public/src/index.js#L167-L179)

* Why were you proud of this piece of code?  
This was the first function in my code that began to grow, and once it was finished I knew it was time to break things out into smaller functions. It was difficult to figure out how to append elements correctly after breaking it out, but I am happy with the end result.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/meloncatty/palette-picker/blob/c281405c3b4f70663e5f3b5acff53c17cc430d25/public/src/index.js#L200-L224)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
The functionality inside of the `try...catch` mirrors the code in my 'happy code'. Instead of creating the element variables inside the 'happy code' it might have been best to pass those variable in as parameters in order to make it more dynamic, thus making the 'sad code' more happy.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

[Material-UI](https://material.io/design/components/text-fields.html)
I like their simple form fields and buttons.

[Material-UI](https://material-ui.com/demos/paper/)
I also like their papers!

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Leta)

### Specification Adherence (out of 50 points): 20 points

* **20 points** - There are two features missing from the base expectations that make the application feel incomplete or hard to use.

Notes:

- Functionality yet to be implemented:
  - Locking functionality
  - On page refresh, the palettes should display in the projects
  - On page refresh, the projects should persist in the dropdown menu
  - Be able to delete palettes
  - If palette in projects is clicked, it should display in main palette

### User Interface (out of 20 points): 15 points

* **15 points** - User interface is mostly intuitive, though the instructor might need some guidance on interactions. Styling is mostly consistent, but could use some clean up. Application may be missing some relevant feedback that would help guide the user.

Notes:

- Palettes saved without a specified project still show up on the screen
- The palettes should be grouped together under the project they're a part of, instead of individual cards that each list a project
- The buttons could use hover states to communicate more to the user
- Nice messaging to indicate success and failure to the user! (It should align more with the functionality - palettes saved without a project should not automatically be appended to the DOM)
- It would be nice if the last selected project remained selected when the palette is saved, so you don't have to re-select the same project if you're creating multiple palettes in it



### Testing (out of 20 points): 7 points

* **7 points** - Project has sporadic testing of some server-side endpoints. There are happy path tests, but there are is one or zero sad path cases.

Notes:

- Testing is incomplete

### Commented Server File (out of 10 points): 0 points

* **10 points** - Each line of the server file (on a separate branch) is commented and explains the code using precise, correct terminology and specificity
* **5 points** - Most lines of the server file (on a separate branch) are commented, but the explanation of code does not display understanding of the underlying code
* **0 points** - Lines are sparsely commented in the server file (on a separate branch) and understanding of the code is clearly lacking

Notes:

- I could not locate the annotated server file; I checked every branch of the repo

### JavaScript Style (out of 30 points): 20 points

* **20 points** - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

### Workflow (out of 20 points): 13 points

* **15 points** - Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of "dead" or commented-out code and debugger statements like console.log that need to be cleaned up.
* **10 points** - Developer(s) make large, inconsistent commits that contain irrelevant changesets and make it difficult to follow the evolution of the application. Developer(s) rarely use git branches and frequently incorporate changes directly into master with little or no review process. There are instances of committed source code that should be .gitignored and instances of dead code and/or debugger statements.

Notes:

- Good number of commits, but git errors make it difficult to follow the evolution of the project coherently

### Project is worth 150 points

### To get a 3 on this project, you need to score 110 points or higher

### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 75 / 150
