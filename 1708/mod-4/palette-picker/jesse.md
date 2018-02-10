# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/jessepackwood/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-jesse-packwood.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/jessepackwood/palette-picker/blob/master/server.js)

## Completion

#### Were you able to complete the base functionality?
No
If not, explain what is missing and why.
I am not able to delete palettes. I started tdd on the server side functionality for delete but did not get to writing the script functions. There is a bug that does not allow some projects to persist. 

#### Which extensions, if any, did you complete?
No extensions
# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/jessepackwood/palette-picker/blob/master/public/js/scripts.js#L112-L123)

* Why were you proud of this piece of code?

It was satifying to use a reduce to structure the data how I wanted to. I used it in order to place the palettes into an array based on the project title.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/jessepackwood/palette-picker/blob/master/public/js/scripts.js#L135-L179)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I didn't have time to refactor this into one function. I was worried about other problems and planned to come back to this for a refactor before submitting it.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()

⚡ mocha


Palette Picker is running on 3000.
  Client Routes
    ✓ should return the homepage (39ms)
    ✓ should return a 404 for a route that does not exist

  API Routes
    GET api/v1/projects
seeding complete
      ✓ should return all the projects
    POST /api/v1/projects
seeding complete
      ✓ should post a new project
seeding complete
      ✓ should return 422 when a required param is missing
    DELETE /api/v1/palettes/:id
seeding complete
      1) should delete a palette
seeding complete
      ✓ should return an error if a palette is not found with the id


  6 passing (182ms)
  1 failing

  1) API Routes
       DELETE /api/v1/palettes/:id
         should delete a palette:

      AssertionError: expected { Object (domain, _events, ...) } to have status code 204 but got 422
      + expected - actual

      -422
      +204

      at chai.request.delete.then.response (test/routes.spec.js:97:32)
      at <anonymous>
      at process._tickCallback (internal/process/next_tick.js:188:7)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

[inspiration](https://codepen.io/robin-dela/pen/QGodeV)

I planned to use this image and populate the saved color palettes like this. I thought it would be fun and unique compared to other palette generators.

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
