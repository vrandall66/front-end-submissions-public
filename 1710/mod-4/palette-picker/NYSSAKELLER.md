# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/nyssakeller/palette-picker)

#### Link to the Deployed Application
[heroku]()

#### Link to your annotated server file
[annotated server file](https://nyssas-rad-palette-picker.herokuapp.com/)

## Completion

#### Were you able to complete the base functionality? 

No. It is missing the lock functionality and the delete functionality. I have a start of how I think the delete functionality should be but I could not get it to work.
The lock functionality I wasn't sure how to do it and I ran out of time while trying to complete other aspets. Also, the corresponding palettes don't show up under their correct project, they just get added to the bottom.
Also, if you add a project or a palette, they show up duplicated until you refresh and I'm not sure why. 

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code]()

* Why were you proud of this piece of code?

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code]()

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

Functions starting at line 68 and line 41. They just don't work right and I dont understand why. It has been very frustrating.
I don't think understand post completely or basically at all. It all felt like a guess and I don't know how to correctly do it. Reading docs online were barely helpful because I couldn't find much.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()
Express intro running on localhost:3000

  ##### Client Routes
    ✓ should return the homepage (74ms)
    ✓ should return a 404 for a route that does not exist

  ##### API Routes
    GET /api/v1/projects
      ✓ should return all of the projects (402ms)
    POST /api/v1/projects
      ✓ should not create a record with missing data
    GET /api/v1/palettes
      ✓ should return all of the palettes
    POST /api/v1/palettes
      1) should not create a record with missing data
      ✓ should return a 404 for a route that does not exist


  6 passing (583ms)
  1 failing

  1) API Routes
       POST /api/v1/palettes
         should not create a record with missing data:

      AssertionError: expected 'Expected format: { \n          name: <String>, \n         color0: <String>, \n          color1: <String>, \n          color2: <String>, \n          color3: <String>, \n          color4: <String>,\n          projects_id: <Number>}. You\'re missing a "name" property.' to equal 'Expected format: { \n name: <String>, \n  color0: <String>, \n  color1: <String>, \n color2: <String>, \n color3: <String>, \n color4: <String>,\n projects_id: <Number>}. You\'re missing a "name" property.}'
      + expected - actual

       Expected format: {
      -          name: <String>,
      -          color0: <String>,
      -          color1: <String>,
      -          color2: <String>,
      -          color3: <String>,
      -          color4: <String>,
      -          projects_id: <Number>}. You're missing a "name" property.
      + name: <String>,
      +  color0: <String>,
      +  color1: <String>,
      + color2: <String>,
      + color3: <String>,
      + color4: <String>,
      + projects_id: <Number>}. You're missing a "name" property.}

      at chai.request.post.send.then.response (test/routes.spec.js:139:36)
      at <anonymous>
      at process._tickCallback (internal/process/next_tick.js:188:7)

#### Link to Design Inspiration

https://dribbble.com/shots/4352131-Sales-Management-Platform-Login-Page

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

I liked the general lay out of this design so I did something similar with mine.

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
