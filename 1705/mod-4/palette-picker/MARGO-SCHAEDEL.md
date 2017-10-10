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
