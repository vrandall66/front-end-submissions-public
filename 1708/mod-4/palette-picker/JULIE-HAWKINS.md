# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/julieahawkins/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-hawk.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/julieahawkins/palette-picker/blob/master/server.js)

## Completion

#### Were you able to complete the base functionality?

I was able to complete the base functionality with exception of clicking on a saved palette and populating the main palette with those saved colors.
I was unable to complete the functionality due to time constraints.
I plan to implement this feature over the weekend.

#### Which extensions, if any, did you complete?
N/A - aiming to include an extension as I continue to work on this project

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/julieahawkins/palette-picker/blob/d64a68a8d9ee0d3ca9ee8c14aa19ea2de54b835c/public/js/scripts.js#L179-L194)

* Why were you proud of this piece of code?
* I was proud of this becuase I did not want to set up a global variable of projects and I wanted to store all my relavent project data in the select options values and text. this allows me to target the id and name of a project without referencing a global variable.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/julieahawkins/palette-picker/blob/d64a68a8d9ee0d3ca9ee8c14aa19ea2de54b835c/public/js/scripts.js#L147-L177)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
* I feel like this function is long and need to be refactored to be cleaner and dryer.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](palette-picker is running on 3000.
  Client Routes
    ✓ should return the homepage with text
    ✓ should return a 404 for a route that does not exist

  API Routes
    GET /api/v1/projects
      ✓ should return all of the projects
    POST /api/v1/projects
      ✓ should create a new project
      - should not create a project with missing data


  4 passing (98ms)
  1 pending)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it
* I found some design inspiration from https://dribbble.com/ as I was perusing projects, I noticed that when you select a project from the main page you are taken to large view of the project with a transparent dark background that exposed the main page behind the view window. I really liked this detail and incorporated it into the view projects functionality for when the user wants to view their saved projects/palettes.

#### Please feel free to ask any other questions or make any other statements below!

I plan to continue working on this project over the weekend to complete the functionality and testing.
I do not feel like this work reflects my best work due to time contraints and the demo competition preparations and I probably didn't time-box as well as I could/should have.

-----


# Instructor Feedback (Instructor Name)

## Specification Adherence

**x points**: (50 possible points)

## User Interface

**x points**: (20 possible points)

## Testing

**x points**: (20 possible points)

## Commented Server File

**x points**: (10 possible points)

## JavaScript Style

**x points**: (30 possible points)

## Workflow

**x points**: (20 possible points)


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
