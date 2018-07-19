# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/seamus-quinn/palette-picker)

#### Link to the Deployed Application
[heroku](https://pickthepaletteduh.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/seamus-quinn/palette-picker/blob/master/server.js)

## Completion

#### Were you able to complete the base functionality?

I did not finish testing.  I had trouble setting up the testing environment.  I now know how to do that and am going to complete my server side testing this weekend.

I also need to display the hex values for the color palettes.

#### Which extensions, if any, did you complete?

None.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/seamus-quinn/palette-picker/blob/971f7f8c531de423348116787b0e0dd705f485aa/public/js/scripts.js#L188-L212)

I made a higher order function that handles everything that happens when a palette is created.  (Appending it to page, posting it to database, then asynchronously giving that dom node a value of the id that was created by the table)

* Why were you proud of this piece of code?

There were a lot of things that needed to happen when a palette is created and I felt that I was able to organize them.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/seamus-quinn/palette-picker/blob/971f7f8c531de423348116787b0e0dd705f485aa/public/js/scripts.js#L129-L158)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I wanted to iterate over the colors and create divs (react style) but couldn't figure out how to do it

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

https://dribbble.com/shots/3446064-Application-Log-in-field

Used the orange from this button to create my generate palettes button

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Leta)

### Specification Adherence (out of 50 points): 35 points

* **40 points** - There is one feature missing from the base expectations that makes the application feel incomplete or hard to use.
* **20 points** - There are two features missing from the base expectations that make the application feel incomplete or hard to use.

Notes:

- Saved palettes don't show up until page refresh (and is a bit idiosyncratic)
- Clicking a saved palette does not cause it to be displayed in the main palette
- Projects with identical names are able to be created

### User Interface (out of 20 points): 12 points

* **15 points** - User interface is mostly intuitive, though the instructor might need some guidance on interactions. Styling is mostly consistent, but could use some clean up. Application may be missing some relevant feedback that would help guide the user.
* **7 points** - User interface demonstrates some effort, but is not intuitive and the instructor needs help figuring out how to use the application. Styling has several inconsistencies and it's sometimes unclear what elements a user can interact with. Application lacks useful feedback for the user.  

Notes:

- The lock buttons don't indicate that the color has been locked
- There is no margin around the projects - could use some breathing room
- The white text against the black background is a bit stressful on the eyes
- The error message when saving a palette without an indivated project is good, but it should be removed once a project is selected
- (As you stated, there are no hex colors displayed)

### Testing (out of 20 points): 0 points

* **0 points** - There is little or no evidence of testing in this application. Most or all of the tests in the test suite are failing.

### Commented Server File (out of 10 points): 8 points

* **10 points** - Each line of the server file (on a separate branch) is commented and explains the code using precise, correct terminology and specificity
* **5 points** - Most lines of the server file (on a separate branch) are commented, but the explanation of code does not display understanding of the underlying code

Notes:

- [Body parser](https://github.com/seamus-quinn/palette-picker/blob/aed7d79debfee56d24a1dbed68779bd7ce9528f7/server.js#L3) is brought in so knex can parse and use the bodies of POST, PUT/PATCH, and DELETE requests
- Did you need to add in the [CORs stuff](https://github.com/seamus-quinn/palette-picker/blob/aed7d79debfee56d24a1dbed68779bd7ce9528f7/server.js#L14-L18)?
- Specifically, [the catch](https://github.com/seamus-quinn/palette-picker/blob/aed7d79debfee56d24a1dbed68779bd7ce9528f7/server.js#L35-L37) runs when the promise is rejected
- Because there is only one [parameter](https://github.com/seamus-quinn/palette-picker/blob/aed7d79debfee56d24a1dbed68779bd7ce9528f7/server.js#L43) in this POST, there is no need to loop through an array of a single element. Instead, just set up a regular if conditional to check that there is a name in the POST.

### JavaScript Style (out of 30 points): 22 points

* **20 points** - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

Notes:

- The saved palettes sometimes show up and sometimes don't. It might be worth using some async awaits to control the code a bit more!

### Workflow (out of 20 points): 19 points

* **20 points** - Developer(s) make many small, atomic commits that clearly document the evolution of the application and do not contain irrelevant changesets that aren't reflected by the commit message. Commit messages are concise and consistent in syntax and tense. Developer(s) effectively use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing directly to master. There are no instances where the developer(s) have committed source code that should be .gitignored. There are no instances of "dead" or commented-out code and debugger statements like console.log.


### Project is worth 150 points

### To get a 3 on this project, you need to score 110 points or higher

### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 96 / 150
