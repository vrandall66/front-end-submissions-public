# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/CamArturo/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-cs.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/CamArturo/palette-picker/blob/master/app.js)

## Completion

#### Were you able to complete the base functionality?

I believe I have most of the functionality. The only thing I am aware of is on the display
of the palettes I don't have the project name. PS The delete works but I need to update the
DOM when you delete until the next page reload.

#### Which extensions, if any, did you complete?

haha

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/CamArturo/palette-picker/blob/a6b6adf063c37bab94f30877b6a313bd2391cc96/public/js/scripts.js#L3-L15)

* Why were you proud of this piece of code?

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code]()

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I have always thought that doing server code was the last step to becoming a full stack developer.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](![image](https://user-images.githubusercontent.com/8752377/42109804-30d77ae4-7b9c-11e8-96a8-780ffd66106d.png)
)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it
(https://colorhunt.co/popular)

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Leta)

### Specification Adherence (out of 50 points): 30 points

* **40 points** - There is one feature missing from the base expectations that makes the application feel incomplete or hard to use.
* **20 points** - There are two features missing from the base expectations that make the application feel incomplete or hard to use.

Notes:

- Multiple projects with the same name can be created.
- Cannot click the saved palette or colors and see them reflected in the larger palette.
- Page refresh required to see saved palettes.
- The submission file is missing pieces - reflection on why you are proud of a piece of your code, a link to a piece of sad code, an explanation of what design inspiration you used.

### User Interface (out of 20 points): 13 points

* **15 points** - User interface is mostly intuitive, though the instructor might need some guidance on interactions. Styling is mostly consistent, but could use some clean up. Application may be missing some relevant feedback that would help guide the user.
* **7 points** - User interface demonstrates some effort, but is not intuitive and the instructor needs help figuring out how to use the application. Styling has several inconsistencies and it's sometimes unclear what elements a user can interact with. Application lacks useful feedback for the user.  

Notes:

- The names of the saved palettes do not show up anywhere (the text near the palette is the project name).
- Project palettes are not grouped together - instead, each individual palette is displayed separately with a project label.
  - Grouping would more clearly indicate the relationship of the saved palettes.
  - As is, it's difficult to see that palettes from a single project belong together.
- The header is an image rather than a logo and text - this is not great from an accessibility standpoint.
- Projects that have no palettes stored in them should be hidden from the dropdown list (aka Turing2 and World).
- Should not be able to create projects whose names are duplicates of existing projects.
- Starting with blank palette squares is confusing; consider starting out with a palette already displaying.
- Main palette is not responsive.
- Lock buttons are clear and intuitive.

### Testing (out of 20 points): 7 points

* **7 points** - Project has sporadic testing of some server-side endpoints. There are happy path tests, but there are is one or zero sad path cases.

NOTES:

- The client side routes should test the content of the HTML being returned.
- The GET for projects should dig into the returned array and check the contents of the first element match what is expected to be returned from the test database.
- The POST test does not cover sad paths.
- The POST test does not examine the contents of the response body.
- There are no tests covering palette creation or recall.

### Commented Server File (out of 10 points): 0 points

* **0 points** - Lines are sparsely commented in the server file (on a separate branch) and understanding of the code is clearly lacking

NOTES:

- No annotations of app.js file on any branch.
- I'm not sure what you are attempting to accomplish with the first of [these two lines](https://github.com/CamArturo/palette-picker/blob/1cf95b8f444d92c3e57a95e71ac353edb001a53a/app.js#L12-L13), since that variable is not used anywhere.
- By convention, [all your variables](https://github.com/CamArturo/palette-picker/blob/1cf95b8f444d92c3e57a95e71ac353edb001a53a/app.js#L19-L21) should go at the top of the file.
- Sometimes your callbacks make use of the streamlined ES6 arrow syntax, but [not always](https://github.com/CamArturo/palette-picker/blob/1cf95b8f444d92c3e57a95e71ac353edb001a53a/app.js#L26) - strive for consistency!
- There is not error handling for if no projects [or palettes](https://github.com/CamArturo/palette-picker/blob/1cf95b8f444d92c3e57a95e71ac353edb001a53a/app.js#L49-L57) exist. Be sure to include good response codes and error messages for handling sad paths.
  - Remember, the catch only triggers if the promise created by querying the database is rejected instead of resolving.
  - If the promise resolves but the contents of the response are not what a developer would expect, you need to create good error messaging to handle that eventuality.

### JavaScript Style (out of 30 points): 20 points

* **20 points** - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

NOTES:

- The [setCSS](https://github.com/CamArturo/palette-picker/blob/1cf95b8f444d92c3e57a95e71ac353edb001a53a/public/js/scripts.js#L34-L69) function has a lot of redundancy and could be dried up by passing in the card and using interpolation.
- When you create a project, there's no validation checking that the project name doesn't already exist.
- When you fetch the projects and [add them as options](https://github.com/CamArturo/palette-picker/blob/1cf95b8f444d92c3e57a95e71ac353edb001a53a/public/js/scripts.js#L85), there's no validation to be sure that projects are being returned from the fetch.


### Workflow (out of 20 points): 13 points

* **15 points** - Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of "dead" or commented-out code and debugger statements like console.log that need to be cleaned up.
* **10 points** - Developer(s) make large, inconsistent commits that contain irrelevant changesets and make it difficult to follow the evolution of the application. Developer(s) rarely use git branches and frequently incorporate changes directly into master with little or no review process. There are instances of committed source code that should be .gitignored and instances of dead code and/or debugger statements.

NOTES:

- Commits are inconsistent - sometimes small, sometimes large and encompassing too many changes.
- Some commented out code remains (before and after hooks in tests)

### Project is worth 150 points

### To get a 3 on this project, you need to score 110 points or higher

### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 83 / 150
