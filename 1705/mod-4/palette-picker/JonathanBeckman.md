# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/jbexx/Palette-Picker)

#### Link to the Deployed Application
[heroku](https://jb-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/jbexx/Palette-Picker/blob/comments/server.js)

## Completion

#### Were you able to complete the base functionality?

If not, explain what is missing and why.

I was able to complete the basice functionality

#### Which extensions, if any, did you complete?

I was able to add the functionality of editing the color value of a single color swatch on the main palette.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
- this is an array of the colors of a specific palette
[happy code](https://github.com/jbexx/Palette-Picker/blob/master/public/js/scripts.js#L62)
- this loops through that array and appends them to the main palette
[happy code](https://github.com/jbexx/Palette-Picker/blob/master/public/js/scripts.js#L146-L153)

* Why were you proud of this piece of code?

Because it took me a while to figure out how to handle an array in a string in html

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/jbexx/Palette-Picker/blob/master/public/js/scripts.js#L179-L190)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I'd like to have these event listeners inline but having to call e.preventDefault because these button are in a form kept me from doing that.  I suppose a point of refactoring would be to move the e.preventDefault into the function Im calling to have the event listeners as one line.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
<img width="452" alt="screen shot 2017-10-08 at 22 52 58" src="https://user-images.githubusercontent.com/23174736/31325546-89de403c-ac7b-11e7-879c-5289754aaf03.png">


[test suite]()

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

Thank you for the extra time.
-----


# Instructor Feedback (Robbie)

## Specification Adherence

**40 points**: (50 possible points)

- I don't see a new project that I created appear on the DOM until I refresh the page
- Minor bug created with extension of editing hex values - if you edit a hex value, then click on a saved palette, the hex colors do not update

## User Interface

**15 points**: (20 possible points)

- The semitransparent rectangle on the front interferes with seeing the colors in the middle - I know you can see below the rectangle, but it would be nice to see all of the full colors, maybe there could be an ability to hide/minimize it

## Data Persistence with SQL Database

**20 points**: (20 possible points)

- Schema looks good with one-to-many relationship using primary/foreign key

## Testing

**15 points**: (20 possible points)

- Roots? `/master/test/roots.spec.js`
- Good job with your before and beforeEach [blocks](https://github.com/jbexx/Palette-Picker/blob/master/test/roots.spec.js#L36-L46)
- For [this test](https://github.com/jbexx/Palette-Picker/blob/master/test/roots.spec.js#L176-L182), you should be testing for an ID that doesn't exist in the database - your current test goes to the standard Express 404 middleware because it expects dynamic IDs to be integers
- Looking for sad paths for POSTs to [projects](https://github.com/jbexx/Palette-Picker/blob/master/test/roots.spec.js#L186) and [palettes](https://github.com/jbexx/Palette-Picker/blob/master/test/roots.spec.js#L216) - for instance for missing data in the body of the request
- [This](https://github.com/jbexx/Palette-Picker/blob/master/test/roots.spec.js#L274) is a good case for a sad path, but would expect a 404 response because the resource does not exist to try to delete in the first place
- Be sure to take [these](https://github.com/jbexx/Palette-Picker/blob/master/test/roots.spec.js#L284) out before you push up code

## Commented Server File

**8 points**: (10 possible points)

- Need to be more specific about variables and what you mean about "multiple servers" [here](https://github.com/jbexx/Palette-Picker/blob/comments/server.js#L9) - a different server doesn't necessarily mean a different environment
- Why ado we need [it](https://github.com/jbexx/Palette-Picker/blob/comments/server.js#L14), though?
- You insert records into [a table](https://github.com/jbexx/Palette-Picker/blob/comments/server.js#L29), not a specific database

## JavaScript Style

**15 points**: (20 possible points)

- Need to be checking that the correct information is giving in the body of the POST request [here](https://github.com/jbexx/Palette-Picker/blob/master/server.js#L29-L31) - check for properties of the request body (never trust the user)
- I would use the plural version of `project` as the return value [here](https://github.com/jbexx/Palette-Picker/blob/master/server.js#L42) because you are most likely returning a collection of projects
- For any route where you are selecting a resource by a dynamic `:id`, you should be able to handle the case where the database does not have that resource in the database and return a 404 status code, for instance this [route](https://github.com/jbexx/Palette-Picker/blob/master/server.js#L60)
- Cool color generation function - I would not [hard code](https://github.com/jbexx/Palette-Picker/blob/master/public/js/scripts.js#L6) `16`, though, and use the length of the string instead in case the string changes for some reason
- For every `fetch()` [call](https://github.com/jbexx/Palette-Picker/blob/master/public/js/scripts.js#L78), you should have a `.catch()` for error handling
- Also, for `fetch()` [calls](https://github.com/jbexx/Palette-Picker/blob/master/public/js/scripts.js#L139), make sure you test for `response.ok` before you parse because fetch does not send 404 responses to the `catch()` method - you have to test the response: https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch#Checking_that_the_fetch_was_successful
- Do you have 4 spaces for your code indentation?

## Workflow

**20 points**: (20 possible points)

- Nice job adding a `.gitignore` in for initial commit

## Extensions

**10 points**: Completed the extension for modifying a color using a hex code


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: 143 / 160
