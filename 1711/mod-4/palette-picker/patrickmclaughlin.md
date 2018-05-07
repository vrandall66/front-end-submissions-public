# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/patrickmc21/palette-picker)

#### Link to the Deployed Application
[heroku](https://palettepickerpat.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/patrickmc21/palette-picker/tree/server-comments)

## Completion

#### Were you able to complete the base functionality?
Yes, basic functionality is completed

If not, explain what is missing and why.

#### Which extensions, if any, did you complete?
none

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/patrickmc21/palette-picker/blob/1406a4df7a774a272575ccfbcc6c525eee76d0fe/public/js/Palette.js#L1-L39)

* Why were you proud of this piece of code?

Organizing the app around a class allowed for easier management of the app. Keeping track of the primary palette as well as the projects with each of their palettes was a much easier task.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/patrickmc21/palette-picker/blob/1406a4df7a774a272575ccfbcc6c525eee76d0fe/public/js/scripts.js#L78-L98)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

This particular block of code features ES5 named functions, ES6 arrow functions in the array prototype, and ES7 async/await. I would like to refactor the app to just be ES6/ES7

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

> palette-picker@1.0.0 test /Users/patrickmclaughlin/turing/Mod4/week1/palette-picker
> NODE_ENV=test mocha --exit



Palette Picker is running on 3000.
  Client Routes
    ✓ should return the homepage
    ✓ should return 404 for a route that does not exist

  API Routes
    GET /api/v1/projects
      ✓ should return all the projects
    GET /api/v1/projects/:id/palettes
      ✓ should return the palettes for given project
      ✓ should return an error if project id is invalid
    POST /api/v1/projects
      ✓ should post a project to the database
      ✓ should not create a project with missing name
    POST /api/v1/projects/:project_id/palette
      ✓ should post a palette to a project
      ✓ should not post a palette if body incomplete
    DELETE /api/v1/projects/:id
      ✓ should delete a project
      ✓ should not delete a project if it has palettes
    DELETE /api/v1/palette/:id
      ✓ should delete a palette
      ✓ should not delete if id is invalid


  13 passing (635ms)



#### Link to Design Inspiration

[button](https://dribbble.com/shots/2839483-Save-Button-Animation)
I liked this design because of the visual feedback it provides to users to show that they have set an action in process. I used it on my save palette and generate new palette buttons

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!
UI design was a challenge, I felt like the only design I liked was very similar to the wireframe as well as the site coolors.

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
