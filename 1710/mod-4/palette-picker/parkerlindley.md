# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/etcetera8/pallete-picker)

#### Link to the Deployed Application
[heroku](https://parkerspalettepicker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/etcetera8/pallete-picker/blob/server-comments/server.js)

## Completion

#### Were you able to complete the base functionality?
Yes

If not, explain what is missing and why.

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/etcetera8/pallete-picker/blob/583b1735d99006520fbec59977d3d0981e506f08/public/js/scripts.js#L148)

* Why were you proud of this piece of code?
I was able to resolve an array of promises almost without thinking about it. I remember struggling to grasp the idea of Promises and promise.all before this mod.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/etcetera8/pallete-picker/blob/master/public/js/scripts.js#L67)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
I wasn't sure if duplicate error handling should be handled in the FE or the BE and juggled between which one to do. I ended up going with what I knew in the sake of time.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
  ```Client Routes
    ✓ should return the homepage
    ✓ should return 404 for page that does not exist

  API Routes
    GET /api/v1/projects
      ✓ should return all of the projects
    POST /api/v1/projects
      ✓ should create a new project
      ✓ should give an error if no project name is given
    GET /api/v1/palettes
      ✓ should get all of the palettes
    GET /api/v1/projects/:id/palettes
      ✓ should get a specific palette for one project
      ✓ should give an error if that project does not exist
    POST /api/v1/palettes
      ✓ should post a new palette to the palettes
      ✓ should return an error if a name is not given
    DELETE /api/v1/palettes/:id
      ✓ should delete a specific palette
      ✓ should return a 404 error if no palette exists
  12 passing```

[test suite](https://github.com/etcetera8/pallete-picker/blob/master/test/routes.spec.js)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it
[wander](https://dribbble.com/shots/1335215-Wander)
I really like the simplicity of the white lined buttons with white text. I copied this and added a hover state to give the user more feedback.
#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

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
