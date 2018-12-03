# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/raualex/palettepicker)

#### Link to the Deployed Application
[heroku](https://palette-picker-ajr.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/raualex/palettepicker/blob/master/server.js)

## Completion

#### Were you able to complete the base functionality?

I was able to complete all of the base functionality, except that I was not able to prevent duplicates to be added to the backend.  I was researching how to do that in the migration, as using a GET with a filter in the JS file was causing buggy behavior, but I ran out of time.

#### Link to an image of your wireframe(s)
[wireframes](https://github.com/raualex/palettepicker) - The wireframe is displayed in the README.

#### Which extensions, if any, did you complete?

I was not able to complete either of the extensions.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/raualex/palettepicker/blob/master/public/js/scripts.js)

* I really liked how I was able to employ for loops to prevent repetitive code in the 'saveColors' and 'postColorsToMainDisplay' functions.  Also, overall, I was happy that my JS had very little buggy behavior and I was able to resue functions and prevent repetitive code as much as possible.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/raualex/palettepicker/blob/master/public/css/styles.css)

* I wish I had more time to make my CSS more responsive.  I used percentages, Flex and Grid to make it relatively responsive, but I wish I had more time to really hammer-down the media queries it needs.

#### Link to Design Inspiration
[Inspiration](https://coolors.co/090909-4b5043-9bc4bc-d3ffe9-8ddbe0)

* Coolers was my basic inspiration for the color blocks on the left hand side of my page.  I thought of Coolers, except making it horizontal, instead of vertical.

#### Please feel free to ask any other questions or make any other statements below!

If at all possible, I would like to go over how to program the migration to decline duplicate info being submitted to the database.  I tried to research using knex to construct a SQL Insert request that avoided duplicates, but I found online that knex did not support that SQL functionality, yet, and doing a GET in the `scripts.js` file and filtering that caused bugs that I could not solve (mainly a variation on the error: `Uncaught (in promise) TypeError: Cannot read property of undefined`).

-----


# Instructor Feedback (Instructor Name)

## Specification Adherence

**x points**: (50 possible points)

## User Interface

**x points**: (20 possible points)

## Commented Server File

**x points**: (10 possible points)

## JavaScript Style

**x points**: (30 possible points)

## Workflow

**x points**: (20 possible points)


### To get a 3 on this project, you need to score 95 points or higher
### To get a 4 on this project, you need to score 115 points or higher

# Final Score: x / 130
