# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project

[palette-picker](https://github.com/andrew-t-james/palette-picker.git)

#### Link to the Deployed Application

[project](https://palette-picker-2018.herokuapp.com/)

#### Link to your annotated server file

[annotated server file](https://github.com/andrew-t-james/palette-picker/blob/annotated-server/server.js)

## Completion

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of

[happy code](https://github.com/andrew-t-james/palette-picker/blob/master/server.js)

- I was happy about building a server with KNEX for the first time.

#### Link to a specific block of your code on GitHub that you feel not great about

[sad code](https://github.com/andrew-t-james/palette-picker/blob/master/public/js/scripts.js)

- I would like to pull out some of the functions into separate smaller single responsibility functions.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
Pallet Picker is running on 3000.
  Client Routes
    ✓ Should return index.html (61ms)
    ✓ Should return a 404 when a route does not exist

  API Routes
    GET /api/v1/projects
      ✓ Should return an array of projects
    GET /api/v1/palettes
      ✓ Should return an array of palettes
    POST to /api/v1/projects
      ✓ Should create a new project
      ✓ Should not create a new project
    DELETE /api/v1/palettes
      ✓ Should delete a palette from the database
      ✓ Should return 422 if palette id does not exist
    POST to /api/v1/palette
      ✓ Should create a new palette
      ✓ Should return 422 if palette id does not exist


  10 passing (891ms)
```

#### Link to Design Inspiration

[Overlapping Circles Dribble Inspiration](https://dribbble.com/shots/4871457-Primary-Maastricht)

---

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
