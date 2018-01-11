UPDATE 17-12-04
Removed comments from server.js
Completed tests for all API endpoints
Removed all linting errors and warnings. 

# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/nicktu12/palette-picker)

#### Link to the Deployed Application
[heroku](https://nt-palettepicker-171201.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/nicktu12/palette-picker/blob/master/server.js)
I accidentally pushed my annotated file to my master branch at 2 a.m. last night. Whoops!

## Completion

#### Were you able to complete the base functionality?

Yes! Base functionality for the application is complete according to project spec. While I was able to successful setup a test environment, I only completed successful tests for one GET endpoint and one POST endpoint. Additionally, the front end is incomplete but all UI interactions are present. 

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/nicktu12/palette-picker/blob/master/server.js)

* Why were you proud of this piece of code?

While not excited about commented out code in the server file, I feel like I learned a lot from building a backend and am very excited to be able to walk through the process of building a backend step by step. 

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/nicktu12/palette-picker/blob/master/public/js/scripts.js)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

Code is not well factored. Using a mix of es5 and es6 syntax. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://github.com/nicktu12/palette-picker/blob/master/test/routes.spec.js)
![screen shot 2017-12-01 at 12 13 09 pm](https://user-images.githubusercontent.com/26471447/33499163-199e6d7a-d691-11e7-842f-e0caebd95e75.png)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

https://codepen.io/TrevorWelch/pen/NwERXE

I wanted to create a ripple effect on the palettes when locked. While I wasn't able to create the ripple at the location of the mouse quick, I was able to quickly implement a knock-off version of the effect. 

#### Please feel free to ask any other questions or make any other statements below!

Really enjoyed learning back-end projects as I was building the project. I felt very strongly about solidifying concepts of the back-end through building one for this project. I am disappointed with my progress on my design and testing, but and happy to have successfully intergrated all user interactions to the front end and wrote a passing GET and POST test. 

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**45 points**: (50 possible points)

* Missing functionality to prevent multiple projects with the same name
* Everything else looks good

## User Interface

**13 points**: (20 possible points)

* The main color palette section looks good, fills the screen, and is easy to use with the lock functionality
* The bottom section with the unstyled form and very small palettes squeezed against the side of the screen is tough to use and read

## Testing

**15 points**: (20 possible points)

* In [this test](https://github.com/nicktu12/palette-picker/blob/master/test/routes.spec.js#L110) and all of the following test, need to return the promise from the chai request (`return chai.request(...)`) in order to not need to use the `done()` callback function in the test
* [This part of your test](https://github.com/nicktu12/palette-picker/blob/master/test/routes.spec.js#L119-L124) can be overkill depending on the dev team you're working on. Some will want the check by making a request, and some will want to assume that unless you get any errors, the DB has done it's thing correctly. Just keep in mind not to nest too many requests or else the test can be difficult to read.
* [This](https://github.com/nicktu12/palette-picker/blob/master/test/routes.spec.js#L196) should be a 404 response
* Overall, good happy and sad path testing

## Commented Server File

**8 points**: (10 possible points)

* [Not just](https://github.com/nicktu12/palette-picker/blob/server-commenting/server.js#L2) at POST, but any request that contains a body
* It isn't just [knex](https://github.com/nicktu12/palette-picker/blob/server-commenting/server.js#L40) that serves everything in an array - it depends on the query you use (if the query asks for a collection of records, then it will return an array)
* Overall, good comments in server file

## JavaScript Style

**22 points**: (30 possible points)

* Don't leave [this](https://github.com/nicktu12/palette-picker/blob/master/server.js#L29) in if you're serving public, static assets
* [This](https://github.com/nicktu12/palette-picker/blob/master/server.js#L39-L46) is a good portion of code where you could refactor into its own function or middleware since you're doing the same thing in another POST request route handler - the only difference is the params that are expected
* Good error handing, but [this](https://github.com/nicktu12/palette-picker/blob/master/server.js#L106) should be a 404 response
(Using [this version](https://github.com/nicktu12/palette-picker/blob/ecd3a0d521c8ec3ea699904c9a2d569a0a5cc5c5/public/js/scripts.js) of your public JS)
* Good job having a `catch()` with each fetch call
* One thing to note with using `fetch` is that it will not error on 404 - in order to hit the `.catch` on a 404, you can check for `response.ok` [demonstrated in the MDN docs here](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch#Checking_that_the_fetch_was_successful)
* Would [break this out](https://github.com/nicktu12/palette-picker/blob/ecd3a0d521c8ec3ea699904c9a2d569a0a5cc5c5/public/js/scripts.js#L89-L92) into its own function
* [Break this out](https://github.com/nicktu12/palette-picker/blob/ecd3a0d521c8ec3ea699904c9a2d569a0a5cc5c5/public/js/scripts.js#L114-L124) into it's own function or even an HTML template

## Workflow

**15 points**: (20 possible points)

* Need much smaller, more atomic commits (should probably be around 100 commits for this project)
* Good job adding a `.gitignore` early on in the project


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 118 / 150
