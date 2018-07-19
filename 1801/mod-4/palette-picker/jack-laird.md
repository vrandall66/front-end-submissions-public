# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/JackLaird0/palette-picker)

#### Link to the Deployed Application
[heroku](https://pallettespickers.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/JackLaird0/palette-picker/tree/annotated-server)

## Completion

#### Were you able to complete the base functionality?

App is completely functional

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/JackLaird0/palette-picker/blob/a30b1cd1c88414bfcda31514025602751f3532ba/server.js#L35)

* Why were you proud of this piece of code?

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/JackLaird0/palette-picker/blob/a30b1cd1c88414bfcda31514025602751f3532ba/test/routes.spec.js#L159)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://i.imgur.com/zss6hhI.png)

#### Link to Design Inspiration

[wire frame](http://frontend.turing.io/assets/images/palette-picker-wireframe.png)
I stole the color scheme and layout

#### Please feel free to ask any other questions or make any other statements below!
Is it necessary to add an aftereach method in your api tests if you're doing roll back at the beforeeach method?

It's a nice catch to have but - not really. The after each is a bit unstable - it doesn't run after a test if the test fails.

-----


# Instructor Feedback (Leta)

### Specification Adherence (out of 50 points): 35 points

* **40 points** - There is one feature missing from the base expectations that makes the application feel incomplete or hard to use.
* **20 points** - There are two features missing from the base expectations that make the application feel incomplete or hard to use.

Notes:

- Submission not complete (no reflections on code)
- When a new project is created, it is not displayed except on page refresh
- Clicking the small project palettes does not display the colors in the main palette

### User Interface (out of 20 points): 12 points

* **15 points** - User interface is mostly intuitive, though the instructor might need some guidance on interactions. Styling is mostly consistent, but could use some clean up. Application may be missing some relevant feedback that would help guide the user.
* **7 points** - User interface demonstrates some effort, but is not intuitive and the instructor needs help figuring out how to use the application. Styling has several inconsistencies and it's sometimes unclear what elements a user can interact with. Application lacks useful feedback for the user.  

Notes:

- The color scheme and fonts make it hard to use/read.
- Many buttons lack hover states that would help make the experience clearer for users.
- The lock/unlock "buttons" are difficult to understand unless you just click on one - not a lot of functionality is communicated by the UI
- Hex codes and Lock button are impossible to read on dark colors
- Project palettes go off the screen and widen the whole page - should implement some sort of wrapping functionality or a horizontal scroll

### Testing (out of 20 points): 15 points

* **15 points** - Project has a running test suite that tests every server-side endpoint, but only has a couple sad path cases.

Notes:

- [This] environment variable should be set in the test script in the package.json: `NODE_ENV=test mocha --exit`
- No sad path for DELETE method
- The seed data for tests should have more than one project and palette, ideally, to ensure that the db is capable of returning arrays of more than one element

### Commented Server File (out of 10 points): 5 points

* **5 points** - Most lines of the server file (on a separate branch) are commented, but the explanation of code does not display understanding of the underlying code

Notes:

- [This](https://github.com/JackLaird0/palette-picker/blob/8cfc80cf3089464beb5211532c6c29969eae8347/server.js#L15) description is too vague and reused
- Annotation on [this](https://github.com/JackLaird0/palette-picker/blob/8cfc80cf3089464beb5211532c6c29969eae8347/server.js#L38-L39) is weak - not sure it's understood what is happening in the code
- [Here](https://github.com/JackLaird0/palette-picker/blob/8cfc80cf3089464beb5211532c6c29969eae8347/server.js#L56) it's better to destructure the project name out of the request body, which means the body can just be `{name: 'project name'}` instead of `{project: {name: 'project name'}}`
- Since there is only one key in the object, there is no need to do [this](https://github.com/JackLaird0/palette-picker/blob/8cfc80cf3089464beb5211532c6c29969eae8347/server.js#L58) - you can just use the if statement

### JavaScript Style (out of 30 points): 22 points

* **20 points** - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

### Workflow (out of 20 points): 15 points

* **15 points** - Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of "dead" or commented-out code and debugger statements like console.log that need to be cleaned up.

Notes:
- For a project this size, I'd expect to see more than ~30 commits to accurately document the project evolution on a granular level

### Project is worth 150 points

### To get a 3 on this project, you need to score 110 points or higher

### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 104 / 150
