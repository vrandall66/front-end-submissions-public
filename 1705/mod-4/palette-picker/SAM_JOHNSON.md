# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the Github Repository for the Project
[palette-picker](https://github.com/sljohnson32/palette-picker)

#### Link to the Deployed Application
[heroku](https://samj-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/sljohnson32/palette-picker/blob/master/server.js)

## Completion

#### Were you able to complete the base functionality?

I was able to get all functionality done as well as add functionality that allows the user to update their previously saved palettes.  This seemed like a logical piece of functionality to provide give then design/goals of the app.

#### Which extensions, if any, did you complete?

I did not complete the provided extensions but I did add functionality as noted above.

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code - testing](https://github.com/sljohnson32/palette-picker/blob/master/test/routes.spec.js)

[happy code - saving updated palettes](https://github.com/sljohnson32/palette-picker/blob/master/public/js/scripts.js)

* Why were you proud of this piece of code?

Testing: I am proud of the testing I was able to get in.  I would have liked to have done a bit more sad path testing but I think my test suite is a good first effort.  

Save Palette function: I am also proud of the additional functionality I added to enable the user to save updated palettes (both colors and the name).  I know that this function could be broken out more than it is currently but I think it's an easy to read and clean piece of code that does a complex task.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/sljohnson32/palette-picker/blob/master/public/js/scripts.js)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I would have ideally spent more time refactoring my code and breaking out functions more and organizing them into different files.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

![test suite](https://github.com/sljohnson32/palette-picker/blob/4236fba346492db0818aec324392b26a55f10f7d/test_results_screenshot.png?raw=true)

#### Please feel free to ask any other questions or make any other statements below!

This was a good project to get back into the swing of things.  I essentially had to relearn jQuery after not using it for almost a year while also learning Express and Knex.  I feel really good about the server side stuff and feel like it's the missing piece for really being able to get a personal project up and running quickly.

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**50 points**: (50 possible points)

- Asked for five colors, not six, but not a big deal...
- Looks like all the features are there (no extensions)

## User Interface

**15 points**: (20 possible points)

- The form is pretty rough to get through - the dropdown has no visual affordance to show it's a dropdown menu

## Data Persistence with SQL Database

**20 points**: (20 possible points)

- Schema looks good with one-to-many relationship using primary/foreign key

## Testing

**17 points**: (20 possible points)

- Good job with the before and beforeEach blocks
- Nice sad path test [here](https://github.com/sljohnson32/palette-picker/blob/master/test/routes.spec.js#L104)
- Would like to see a sad path test for a [deletion](https://github.com/sljohnson32/palette-picker/blob/master/test/routes.spec.js#L199) with an incorrect ID

## Commented Server File

**5 points**: (10 possible points)

- Good high-level overview of the chunks of code, but looking for specificity on each line

## JavaScript Style

**13 points**: (20 possible points)

- [Ordering results](https://github.com/sljohnson32/palette-picker/blob/master/server.js#L20) can be OK for smaller datasets, but imagine you have thousands of records; it will take a long time to sort them and slow down your API
- [This](https://github.com/sljohnson32/palette-picker/blob/master/server.js#L24) is ok, but usually you will just see an empty array as a response
- [This section](https://github.com/sljohnson32/palette-picker/blob/master/server.js#L113-L119) and [this section](https://github.com/sljohnson32/palette-picker/blob/master/server.js#L89-L95) are very similar in structure, see if you can refactor this to DRY it up
- I like the extraction of fetch calls into [another file](https://github.com/sljohnson32/palette-picker/blob/master/public/js/fetch.js) - I suppose I would call the filename something different because it sounds like a polyfill for fetch or source code
- Make sure every `fetch()` call has a `.catch()`
- Do not use ID attributes to store data about resources, rather use the [DATA attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/data-*)
- [This block](https://github.com/sljohnson32/palette-picker/blob/master/public/js/scripts.js#L165-L201) is getting quite long and tough to parse

## Workflow

**20 points**: (20 possible points)

- Nice small commits - good job adding .gitignore right off the bat


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: 140 / 160
