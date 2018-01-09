# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/rufusasterisk/palette-picker/)

#### Link to the Deployed Application
[heroku](https://rufus-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file]() - coming soon

## Completion

#### Were you able to complete the base functionality?
No.

If not, explain what is missing and why.
The lock feature is not working. The software does not block users from creating projects with duplicate names.
My server file is not commented

I built the color picker using HSL instead of RGB or Hex, mostly because I've never worked with HSL and converting between the two is cool math.
The HSL requires a variety of conversions and varying dom manipulation. I ran out of time after spending time on the color functions plus the time spent on Demo night

#### Which extensions, if any, did you complete?

Application generates random color palettes using tetrachromatic theory for the first 4 colors. HSL made this trivial.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/rufusasterisk/palette-picker/blob/master/public/js/colorHelpers.js#L37-L151)

* Why were you proud of this piece of code?

There are a few functions in this block of code - they convert hexadecimal colors to HSL colors and HSL to hex.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/rufusasterisk/palette-picker/blob/master/public/js/scripts.js#L124-L159)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

it's a 35 line function with a lot of repeated code. I had to spend time on other parts of the app and didn't have time to refactor.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]() - coming soon - suite does not run, pages of errors

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it - coming soon

#### Please feel free to ask any other questions or make any other statements below!

I'm frustrated at the state of this app. I've worked 12hrs+ every day this week and it's in a terrible state.

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**40 points**: (50 possible points)

* Lock is missing
* Don't see any link to design inspiration you used for this site

## User Interface

**13 points**: (20 possible points)

* There is some default project's palettes being shown, but it's unclear while. There is no title, and the drop-down menu says No Project Selected. Looks like all palettes, but would be nice to have a cue.
* A lot of unused space in the bottom of the page. Even filling that with the palette colors would be nice.

## Testing

**0 points**: (20 possible points)

* [This file](https://github.com/rufusasterisk/palette-picker/blob/master/test/routes.spec.js) is commented out and does not have any API testing functionality.
* Sent a screenshot of the client-side tests passing - only client-side testing running.

## Commented Server File

**0 points**: (10 possible points)

* Not done

## JavaScript Style

**22 points**: (30 possible points)

* You should not need `return` every time you want to send a response in a route handler - you should only need an explicit return if you are in an if/else where it is explicitly needed.
* Good job extracting [this functionality](https://github.com/rufusasterisk/palette-picker/blob/master/server.js#L70-L79) into its own function
* If you make the `checkPostBody` a middleware function, then you can get rid of [this if/else section](https://github.com/rufusasterisk/palette-picker/blob/master/server.js#L82-L85) because you would return an error response if there was something missing within the middleware - if nothing is missing, then you move on to the route handler as normal, which removes the conditional. You'll just have to find a way to pass the array of necessary parameters into the middleware.
* Server file looks good - routes are RESTful, and database queries are simple
* As you said, cleint-side code definitely needs some refactoring
* One thing to note with using `fetch` is that it will not error on 404 - in order to hit the `.catch` on a 404, you can check for `response.ok` [demonstrated in the MDN docs here](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch#Checking_that_the_fetch_was_successful)

## Workflow

**17 points**: (20 possible points)

* Your `.gitignore` is empty...do you have one globally?
* Would like to see some smaller commits

## Extensions

**15 points:** Palette generation that isn’t random and actually makes sense

* [This](https://github.com/rufusasterisk/palette-picker/blob/master/public/js/colorHelpers.js) is cool


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 107 / 150
