# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/EricMellow/palette-picker)

#### Link to the Deployed Application
[heroku](https://mellow-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/EricMellow/palette-picker/blob/server-comments/server.js)

## Completion

#### Were you able to complete the base functionality?

Although a little buggy, it does have all of the base functionality. Wait, I was just reminded that you are supposed to be able to click on the palette under its project name and have the main palette change to those colors. I forgot about that, so it definitely doesn't have that bit of functionality. Oops!

#### Which extensions, if any, did you complete?

Hahaha!

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/EricMellow/palette-picker/blob/702039f859b4403f18f3c6f85a85545c6c32a024/server.js#L114-L128)

* I liked that I was able to implement the dynamic route feature to get all of the palettes from a specific project. I did this late in the project, and wish I had put more of my logic in the server.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/EricMellow/palette-picker/blob/702039f859b4403f18f3c6f85a85545c6c32a024/public/js/scripts.js#L164-L207)

* This is ugly and there's another function that kind of has some similar functionality, so I don't feel good about that. Definitely doesn't feel like DRY code. Refactor?! HA! I definitely didn't have time refactor.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://github.com/EricMellow/palette-picker/blob/master/public/assets/Screen%20Shot%202018-06-29%20at%208.45.22%20AM.png)

#### Link to Design Inspiration

* I scrolled through dribble a bit, but it was kind of overwhelming and I didn't really find anything useful. Honestly, I never got to a place during this project where I had time to go look for design inspiration.

#### Please feel free to ask any other questions or make any other statements below!

I'm sleepy!

-----


# Instructor Feedback (Leta)

### Specification Adherence (out of 50 points): 43 points

* **50 points** - No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use. Data persists on refresh using a knex/postgreSQL database.
* **40 points** - There is one feature missing from the base expectations that makes the application feel incomplete or hard to use.

Notes:

- Even though projects with duplicate names are not being added to the database, the duplicated project shows up on the UI until the page is refreshed
- When I click an existing palette, it does not get displayed in the main palette cards

### User Interface (out of 20 points): 18 points

* **20 points** - User interface is intuitive and the instructor can easily use it on their own without guidance. Styling is consistent and call-to-action elements are obvious. The application provides the user with relevant feedback based on interactions.  

Notes:

- The palette cards expand when you lock them to accommodate the "Locked" script. I'd recommend using a max-width or minmax() to prevent that warping.
- It'd be great to have a more explicit success visual when projects and palettes are created.
- The cursive display font should probably not be used for the project and palette titles - a more readable option would be to use the body text font but in a heavier weight.

### Testing (out of 20 points): 10 points

* **15 points** - Project has a running test suite that tests every server-side endpoint, but only has a couple sad path cases.
* **7 points** - Project has sporadic testing of some server-side endpoints. There are happy path tests, but there are is one or zero sad path cases.

Notes:

- [This](https://github.com/EricMellow/palette-picker/blob/83431717cf6e395107feeb4c7f8404f67913b53d/test/routes.spec.js#L11) description is misleading; the response is HTML, not a string
- Why are the callbacks [here](https://github.com/EricMellow/palette-picker/blob/83431717cf6e395107feeb4c7f8404f67913b53d/test/routes.spec.js#L34-L45) ES5 instead of arrow functions like the rest of your code?
- [This](https://github.com/EricMellow/palette-picker/blob/83431717cf6e395107feeb4c7f8404f67913b53d/test/routes.spec.js#L47-L60) project creation endpoint test should also double check that the name of "Test" is being added to the database, not just the ID
- Why are [these lines](https://github.com/EricMellow/palette-picker/blob/83431717cf6e395107feeb4c7f8404f67913b53d/test/routes.spec.js#L71-L72) commented out?
- No sad path for posting a new palette
- No testing for DELETE method

### Commented Server File (out of 10 points): 6 points

* **10 points** - Each line of the server file (on a separate branch) is commented and explains the code using precise, correct terminology and specificity
* **5 points** - Most lines of the server file (on a separate branch) are commented, but the explanation of code does not display understanding of the underlying code

Notes:

- [These lines](https://github.com/EricMellow/palette-picker/blob/7fe851ea60b71e063c2d695a8ee25dfaedb9c6c6/server.js#L14-L17) are more specifically telling the app to serve up the resources it finds in the public directory when the root ('/') is requested, and allowing knex to parse the request body of POST and DELETE requests, respectively.
- A good alternative to [using async await and querying the server every time you want to create a new project](https://github.com/EricMellow/palette-picker/blob/7fe851ea60b71e063c2d695a8ee25dfaedb9c6c6/server.js#L31) is to store the existing projects in app.locals and just checking through an array of strings :) And then if there's no match, add the new project to the database and update the array of project names in app.locals.
- A `.catch()` will specifically run when _the promise is rejected_ - not just when a nebulous error occurs.

### JavaScript Style (out of 30 points): 20 points

* **20 points** - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

### Workflow (out of 20 points): 20 points

* **20 points** - Developer(s) make many small, atomic commits that clearly document the evolution of the application and do not contain irrelevant changesets that aren't reflected by the commit message. Commit messages are concise and consistent in syntax and tense. Developer(s) effectively use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing directly to master. There are no instances where the developer(s) have committed source code that should be .gitignored. There are no instances of "dead" or commented-out code and debugger statements like console.log.


### Project is worth 150 points

### To get a 3 on this project, you need to score 110 points or higher

### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 117 / 150
