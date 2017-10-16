# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/mschae16/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-mjs.herokuapp.com)

#### Link to your annotated server file
[annotated server file](https://github.com/mschae16/palette-picker/tree/server-comments)

## Completion

#### Were you able to complete the base functionality?

Yes, I was able to complete the base functionality.

#### Which extensions, if any, did you complete?

No extensions.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/mschae16/palette-picker/blob/master/public/js/scripts.js#L131-L150)

* Why were you proud of this piece of code?

After writing the functions for appending an individual project and palette to the DOM, when adding in page load functionality, I realised that I could write just one fetch function and pass in the necessary path and append method, dependent on whether I am trying to fetch projects or palettes, and then I could just re-use the append functions already created without having to create brand new functions for appending all projects and palettes to the DOM. I'm happy that I was able to re-use previously written code, and cut down the necessity to write repetitive code.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/mschae16/palette-picker/blob/master/public/js/scripts.js#L117-L129)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

This link for my sad code references my script file, specifically, but what I was really frustrated with extends to an issue larger than just this chunk of code.  What I was unhappy with was, when having to send palettes to the database, I had to send in the five hex values as separate strings rather than sending in an array, and storing it in the database as an array. I know Postgres/Knex traditionally did not support storage of arrays and there is a lot of backlash over the move to support storage of arrays, but to me, I believe it would have made writing the frontend code cleaner and more concise.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://slack-files.com/T029P2S9M-F7EHK4HQT-4e3374558f)

All 12 tests passing.

#### Please feel free to ask any other questions or make any other statements below!

Backend testing is awesome (compared to frontend testing)!

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**45 points**: (50 possible points)

- Minor missing feature for when you click on a saved palette, and it should show the palette again (with the large colors)

## User Interface

**15 points**: (20 possible points)

- Look to add some kind of prevent default on the left container, because if you press spacebar while focused in there, then it scrolls to the bottom
- Form is similar to the wireframe, which is hard to parse and know exactly what to do first. Do I need to create a project in order to save a palette?

## Data Persistence with SQL Database

**20 points**: (20 possible points)

- Schema looks good with one-to-many relationship using primary/foreign key

## Testing

**15 points**: (20 possible points)

- Skipped test, not sure exactly why
- Be consistent on using double vs. single quotations [for strings](https://github.com/mschae16/palette-picker/blob/master/test/routes.spec.js#L6)
- Good job with your before and beforeEach blocks
- [This 404 test](https://github.com/mschae16/palette-picker/blob/master/test/routes.spec.js#L109) and [this test](https://github.com/mschae16/palette-picker/blob/master/test/routes.spec.js#L68) are actually testing the same mechanism in Express to handle unknown routes, so you only need to test this once
- Good sad path [test](https://github.com/mschae16/palette-picker/blob/master/test/routes.spec.js#L144) and [here](https://github.com/mschae16/palette-picker/blob/master/test/routes.spec.js#L238)
- Are you actually testing for "incorrect" data [here](https://github.com/mschae16/palette-picker/blob/master/test/routes.spec.js#L204), or just missing data?

## Commented Server File

**8 points**: (10 possible points)

- Missing the details around explanation of the knex config section
- Some good, details comments 
- Not sure about the wording for `consume` a promise, you're really just calling `.then()`

## JavaScript Style

**15 points**: (20 possible points)

- Group all of the `projects` routes together, and then group all of the `palettes` routes together because it's easier to see what resources have what functionality
- [This section](https://github.com/mschae16/palette-picker/blob/master/server.js#L37-L39) and [this section](https://github.com/mschae16/palette-picker/blob/master/server.js#L57-L62) have very similar functionality. See how you can pull out the functionality and maybe create one piece of middleware to DRY up the server code.
- Once you're using a [multi-line ternary](https://github.com/mschae16/palette-picker/blob/master/server.js#L77-L80), why not just use an if/else - ternaries are usually harder to parse for other developers - and [here](https://github.com/mschae16/palette-picker/blob/master/public/js/scripts.js#L24-L27)
- Cool color picking [logic](https://github.com/mschae16/palette-picker/blob/master/public/js/scripts.js#L2)
- Instead of using the `id` [attribute](https://github.com/mschae16/palette-picker/blob/master/public/js/scripts.js#L36), use `data` attributes to store data about a DOM node, same with palettes
- Good check [here](https://github.com/mschae16/palette-picker/blob/master/public/js/scripts.js#L62)
- A good error check [here](https://github.com/mschae16/palette-picker/blob/master/public/js/scripts.js#L173), but not a very helpful response for the user
- Why the [newline](https://github.com/mschae16/palette-picker/blob/master/public/js/scripts.js#L211)?

## Workflow

**20 points**: (20 possible points)

- Great small commits using imperative subject lines with a lot of branches - keep it up


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: 133 / 160
