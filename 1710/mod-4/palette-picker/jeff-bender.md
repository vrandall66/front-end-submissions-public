# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/j25bender/palette-picker)

#### Link to the Deployed Application
[heroku](https://penta-chroma.herokuapp.com/)

#### Link to your annotated server file
Still working on this...
[annotated server file](https://github.com/j25bender/palette-picker/blob/feature/server-comments/server.js)

## Completion

#### Were you able to complete the base functionality?
Yes

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/j25bender/palette-picker/blob/master/public/index.html)

* Why were you proud of this piece of code?
Lines 12 - 26
I utilized <polygon> elements to produce the pentagram color palette.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/j25bender/palette-picker/blob/master/public/js/scripts.js)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
Lines 30 - 35
There's some code here that looks like it could be refactored to be more DRY.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
Client Routes
    ✓ GET Should return homepage with text
    ✓ GET Requesting a non-existent path should return 404

  API Routes
    GET /api/v1/projects
Seeding TEST data complete!
      ✓ Should return all of the projects
    GET /api/v1/projects/:id
Seeding TEST data complete!
      ✓ Should return a project by id
    GET /api/v1/projects/:id/palettes
Seeding TEST data complete!
      ✓ Should return all of the palettes of a project
    POST /api/v1/projects
Seeding TEST data complete!
      ✓ Should create a new project
Seeding TEST data complete!
      ✓ POST Should NOT create a new project if there is no title
    POST /api/v1/palettes
Seeding TEST data complete!
      ✓ Should create a new palette
Seeding TEST data complete!
      ✓ POST Should NOT create a new palette if there is no name
    DELETE /api/v1/palettes/:id
Seeding TEST data complete!
      ✓ Should delete a palette by id
Seeding TEST data complete!
      ✓ Should NOT delete a palette if id doesn't exist

  11 passing (620ms)

#### Link to Design Inspiration
https://en.wikipedia.org/wiki/Theory_of_Colours#/media/File:Goethe,_Farbenkreis_zur_Symbolisierung_des_menschlichen_Geistes-_und_Seelenlebens,_1809.jpg* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

#### Please feel free to ask any other questions or make any other statements below!
Thanks for the additional help finishing up this project!
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
