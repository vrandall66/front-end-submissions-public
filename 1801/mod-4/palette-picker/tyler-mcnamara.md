# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/mcnamara14/palette-picker)

#### Link to the Deployed Application
[heroku](https://tylers-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/mcnamara14/palette-picker/blob/master/server.js)

## Completion

#### Were you able to complete the base functionality?

If not, explain what is missing and why.

I was not able to fully test the app or complete the design so it was mobile friendly and bug free. I did get close however. This was the first time I felt I truly didn't have enough time to get the project done because of my computer breaking Monday and working on my app for Demo Comp as well as the time it took to present at Demo Comp. I really don't like not turning in a completely polished project so hoping to work on it this weekend so it is.

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/mcnamara14/palette-picker/blob/master/public/js/scripts.js#L152)

* Why were you proud of this piece of code?

I was happy to have found a way to add the project id to the project div and then find a way to pull that id for database purposes.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/mcnamara14/palette-picker/blob/master/public/js/scripts.js#L196)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I am not happy with the amount of code it took to create on html element, I would like to refactor, most likely through a loop, so that it looks much more clean.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://user-images.githubusercontent.com/479463/42109734-eafba2a2-7b9b-11e8-823e-7acd289c0917.png)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

[adobe kuler](https://color.adobe.com/create/color-wheel/)

#### Please feel free to ask any other questions or make any other statements below!

I really enjoyed this project and learning the backend. Would love the opportunity to spend a little more time on making sure it's complete.

-----


# Instructor Feedback (Leta)

### Specification Adherence (out of 50 points): 40 points

* **40 points** - There is one feature missing from the base expectations that makes the application feel incomplete or hard to use.

Notes:

- Duplicate project names can be created
- Clicking the saved palettes does not make them display in the larger palette

### User Interface (out of 20 points): 14 points

* **15 points** - User interface is mostly intuitive, though the instructor might need some guidance on interactions. Styling is mostly consistent, but could use some clean up. Application may be missing some relevant feedback that would help guide the user.
* **7 points** - User interface demonstrates some effort, but is not intuitive and the instructor needs help figuring out how to use the application. Styling has several inconsistencies and it's sometimes unclear what elements a user can interact with. Application lacks useful feedback for the user.  

Notes:

- The very dark color scheme and low-contrast buttons/text makes the app difficult to read
- Adding hover states to the buttons would improve the feedback for the user, particularly with the locks
- The form to name the palette is separated from the colors by that horizontal rule and makes it difficult to intuitively understand how they connect together
- When a palette was deleted, the page stopped displaying the entire project. It came back on page refresh.
- No error messaging telling the user that they can't save a palette without putting it in a project

### Testing (out of 20 points): 0 points

* **0 points** - There is little or no evidence of testing in this application. Most or all of the tests in the test suite are failing.

### Commented Server File (out of 10 points): 0 points

* **0 points** - Lines are sparsely commented in the server file (on a separate branch) and understanding of the code is clearly lacking

### JavaScript Style (out of 30 points): 18 points

* **20 points** - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.
* **10 points** - Your application has a significant amount of duplication and one or more major bugs. Developer cannot speak to most choices and does not know what every line of code is doing.

Notes:

- Organization of variables, functions, invocations, and event listeners makes it difficult to understand what's going on in the code


### Workflow (out of 20 points): 12 points

* **15 points** - Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of "dead" or commented-out code and debugger statements like console.log that need to be cleaned up.
* **10 points** - Developer(s) make large, inconsistent commits that contain irrelevant changesets and make it difficult to follow the evolution of the application. Developer(s) rarely use git branches and frequently incorporate changes directly into master with little or no review process. There are instances of committed source code that should be .gitignored and instances of dead code and/or debugger statements.

Notes:

- It looks like you had under 20 commits excluding the deployment commits. That's really not enough to accurately reflect the evolution of a project on a granular level


### Project is worth 150 points

### To get a 3 on this project, you need to score 110 points or higher

### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 84 / 150
