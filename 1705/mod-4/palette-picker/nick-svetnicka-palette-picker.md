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


# Instructor Feedback (Robbie)

## Specification Adherence

**50 points**: (50 possible points)

- Looks like all the features are there (no extensions)

## User Interface

**15 points**: (20 possible points)

- The form is roughly styled and hard to follow
- The colors could use up more real estate; they are pretty small, which is a little frustrating for the user since the colors are the central purpose of the site
- Good job have a `There are no saved palettes.` as a placeholder

## Data Persistence with SQL Database

**20 points**: (20 possible points)

- Schema looks good with one-to-many relationship using primary/foreign key
- I haven't used the json column type before, I wonder how that worked out, any issues?

## Testing

**17 points**: (20 possible points)

- Good job with the before and beforeEach blocks
- [This test](https://github.com/EndlessHypnosis/palette-picker/blob/master/test/endpoints.spec.js#L130-L163) is very thorough, I'm wondering if it's too thorough; is the first request really necessary if you trust your seed file is running (and you don't modify your seed data - either way the test is fragile)
- Watch out for [typos](https://github.com/EndlessHypnosis/palette-picker/blob/master/test/endpoints.spec.js#L167)
- Would want to see a sad path test for [this route](https://github.com/EndlessHypnosis/palette-picker/blob/master/test/endpoints.spec.js#L252) for when you try to delete an item that does not exist in the DB

## Commented Server File

**8 points**: (10 possible points)

- Want to see some more specificity in terminology, for instance the reasoning behind the specific body parser settings [here](https://github.com/EndlessHypnosis/palette-picker/blob/server-js-comments/server.js#L13)

## JavaScript Style

**15 points**: (20 possible points)

- Helpful error handling [here](https://github.com/EndlessHypnosis/palette-picker/blob/master/server.js#L47)
- Status 201 [here](https://github.com/EndlessHypnosis/palette-picker/blob/master/server.js#L71) for an error?
- [This](https://github.com/EndlessHypnosis/palette-picker/blob/master/public/js/scripts.js#L52-L89) is brutal in terms of readability - needs refactoring
- Instead of using the name of a project as an ID attribute in your HTML, you can use the data HTML attribute to store data information about an element, an ID is traditionally used for styling and targeting specific elements for JS hooks
- Are you really accepting all content types? Your implementation seems to depend on getting JSON back as a response
- Seems like you could tie [these classes](https://github.com/EndlessHypnosis/palette-picker/blob/master/public/js/scripts.js#L212-L213) together into one "locked" class, and then just toggle it

## Workflow

**17 points**: (20 possible points)

- Try for some smaller commits along the way, overall pretty good
_ nice job adding .gitignore right off the bat

### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: 142 / 160
