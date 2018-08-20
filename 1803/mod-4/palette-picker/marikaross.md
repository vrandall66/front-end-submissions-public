# Palette Picker Submission Form

[[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/marikaross/palette-picker)

#### Link to the Deployed Application
[[heroku](https://so-many-colors.herokuapp.com)

#### Link to your annotated server file
[annotated server file](https://github.com/marikaross/palette-picker/pull/8)

## Completion

#### Were you able to complete the base functionality?

You are still able to put multiple folders of the same name in the database.  I simply ran out of time.

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/marikaross/palette-picker/blob/master/public/scripts.js)
line 97-136
* Why were you proud of this piece of code?
I had actually started this trying to do a fetch call the palette.project_id endpoint.  I had wanted to make an entire object with all of the required info and then map over it and append the info, but I kept getting a bunch of unresolved promises that I couldn't resolve.  I ended up reducing my fetch calls to 2 and my program worked faster and I still got the info I needed. 

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/marikaross/palette-picker/blob/master/public/scripts.js)


* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
lines 58-76 because this was an inconsistency in using async await and .then.catch.  I should have just used one.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
undefined is running on 3000.
  ```GET to /api/v1/projects
Seeding complete!
    ✓ should return all projects
Seeding complete!
    ✓ should return a 404 for a route that does not exist

  GET to /api/v1/palettes
Seeding complete!
    ✓ should return all palettes
Seeding complete!
    ✓ should return a 404 for a route that does not exist

  POST /api/v1/projects
Seeding complete!
    ✓ should add a project
Seeding complete!
    ✓ should not create an entry if data is missing

  POST /api/v1/projects
Seeding complete!
    ✓ should add a palette
Seeding complete!
    ✓ should not create an entry if data is missing

  GET to /api/v1/projects/:id
Seeding complete!
    ✓ should return a single project
Seeding complete!
    ✓ should return a 404 for a route that does not exist

  GET /api/v1/palettes/:id
    ✓ should return a single palette

  DELETE api/v1/palettes/:id
Seeding complete!
    ✓ should delete a single palette from the database


  12 passing (829ms)```
[test suite](https://github.com/marikaross/palette-picker/blob/master/test/routes.spec.js)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it
[colormind.io](http://colormind.io/)
I stole the basic design from it (background color, font, I wanted to copy the buttons but forms are impossible to style).  Despite being a front-end developer, I really struggle with creating design concepts on my own. 
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
