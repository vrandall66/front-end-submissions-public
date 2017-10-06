# Palette Picker Submission Form
## Nick Svetnicka
## Mod 4 FE-1705

> Execution Notes:

- the 2 databases should be called palettepicker and palettepicker_test

- I setup the testing on port 3001, so to run the test suite, run: **npm run test**

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/EndlessHypnosis/palette-picker)

#### Link to the Deployed Application
[heroku](https://ns-palette-picker.herokuapp.com)

#### Link to your annotated server file
[annotated server file](https://github.com/EndlessHypnosis/palette-picker/blob/server-js-comments/server.js)

## Completion

#### Were you able to complete the base functionality?

> YES! I think I completed all of the functionality requirements.

#### Which extensions, if any, did you complete?

> No official extensions, but you'll notice a few niceties...plenty of error handling, default values when no palettes/projects exist...just small UX improvements...again NO OFFICAL EXTENSION ;)

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/EndlessHypnosis/palette-picker/blob/master/public/js/scripts.js#L31-L92)

> NOTE: _same block used for both answers (happy and sad block )_

** Why were you proud of this piece of code? **

> This is a pretty complex function here. There are 3 nested forEach statements, uses array prototypes reduce and filter. And also has alot of dynamic DOM element creation. Overall, I'm proud of this beast because it's pulling off some pretty neat stuff...but see next section for the sad part...

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/EndlessHypnosis/palette-picker/blob/master/public/js/scripts.js#L31-L92)

> NOTE: _same block used for both answers (happy and sad block )_

** Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it? **

> I just didn't have the time to refactor this. There are clearly defined sections of logic within the entire function, and could easily be broken out into separate functions. What's tricky is the 3 nested forEaches, and moreso, all the DOM element creation that it's doing. Just didn't have the time to refactor, but I **really really** hate having functions this huge :(


#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://github.com/EndlessHypnosis/palette-picker/blob/master/public/images/palette_picker_tests.png)

#### Please feel free to ask any other questions or make any other statements below!

> There is NO seed data for DEV..only TEST environment. This is intentional to demonstrate application state with 0 projects/ 0 palettes.

> The biggest area I struggled, and could use some guidance on is when sending back a response from an endpoint, when to use .status().send() vs .status().json(). Also, this impacts how the consumer of these endpoints work with the response.

-----


# Instructor Feedback (Instructor Name)

## Specification Adherence

**x points**: Lorem ipsum dolor set amet

## User Interface

**x points**: Lorem ipsum dolor set amet

## Data Persistence with SQL Database

**x points**: Lorem ipsum dolor set amet

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**x points**: Lorem ipsum dolor set amet


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: x / 160
