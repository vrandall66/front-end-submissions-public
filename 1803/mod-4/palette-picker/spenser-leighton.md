# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/spenserleighton1/pallete-picker)

#### Link to the Deployed Application
[heroku](https://spenser-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/spenserleighton1/pallete-picker/blob/serverNotes/server.js)

## Completion

#### Were you able to complete the base functionality?
Yes!

If not, explain what is missing and why.

#### Which extensions, if any, did you complete?
Not on the extensions list, but I added an option to delete an entire project.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/spenserleighton1/pallete-picker/blob/826f3967292ab9a59856c2b7b1c6c23a953647b7/public/scripts.js#L88)

I enjoyed the error handling in the form inputs.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/spenserleighton1/pallete-picker/blob/826f3967292ab9a59856c2b7b1c6c23a953647b7/public/scripts.js#L19)

I don't like this global variable. Really though, a lot of my code makes me sad. I wish I would have set aside time to refactor it. All of the functionality is there, it just gets a little sloppy.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

Palette Picker is running on 3000.
  Client facing routes
Seeding complete!
    ✓ should display html at root
Seeding complete!
    ✓ should return 404 on sad path

  GET api/v1/projects
Seeding complete!
    ✓ should return all projects

  GET spi/v1/projects/:id
Seeding complete!
    ✓ should return a single project

  GET api/v1/palettes
Seeding complete!
    ✓ should return all palettes

  GET api/v1/palettes/id
Seeding complete!
    ✓ should return a single palette

  POST api/v1/projects
Seeding complete!
    ✓ should add Project
Seeding complete!
    ✓ should error if title is missing

  POST api/v1/palettes
Seeding complete!
    ✓ should add a palette
Seeding complete!
    ✓ should error if title is missing

  DELETE /api/v1/palettes/:id
Seeding complete!
    ✓ should remove a palette from the database

  DELETE /api/v1/palettes/:project_id
Seeding complete!
    ✓ should remove all palettes matching foreign id from the database


  12 passing (732ms)


#### Link to Design Inspiration

[design](https://dribbble.com/shots/4810664-Free-Youtube-Subscribe-Button-Png-Download-By-AlfredoCreates-7)
I liked the red arrow, I wanted to animate it though...

#### Please feel free to ask any other questions or make any other statements below!

This was fun! Definitely more difficult (on the FE) thn I anticipated. Next time my jQuery won't be so ugly!

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
