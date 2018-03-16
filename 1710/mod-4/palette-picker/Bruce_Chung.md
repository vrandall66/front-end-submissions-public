# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/brucekchung/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-bruce.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/brucekchung/palette-picker/blob/comments/server.js)

## Completion

#### Were you able to complete the base functionality?

Missing refresh on delete, although the database removes the palette and makes correct changes on refresh.
Clicking on palette does not load into main.

Alibi: split attention on job search

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
second migration:
[happy code](https://github.com/brucekchung/palette-picker/blob/master/db/migrations/20180315080632_add-array.js)

* Why were you proud of this piece of code?

was glad to be able to edit the schema of the db

#### Link to a specific block of your code on GitHub that you feel not great about

pleased about the code I wrote, sad that I didn't write all the code I need
[sad code]()

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
brucechung@Bruces-MacBook-Pro:~/Documents/turing/mod4/palette-picker 🌏  npm test

> palette-picker@1.0.0 test /Users/brucechung/Documents/turing/mod4/palette-picker
> NODE_ENV=test mocha --exit



listening on 3000
  Client Routes
    ✓ should return the homepage with text
    ✓ should return a 404 if the path does not exist

  API Routes
    GET /api/v1/projects
      ✓ should return all of the projects
    POST /api/v1/projects
      ✓ should be able to add a project
      ✓ should return an error if data is missing
    GET /api/v1/palettes
      ✓ should return all the palettes
    POST /api/v1/palettes
      ✓ should be able to post a palettes
      ✓ should return an error if data is missing
    DELETE /api/v1/palettes
      - should be able to delete a palette


  8 passing (436ms)
  1 pending
```
[test suite]()

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

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
