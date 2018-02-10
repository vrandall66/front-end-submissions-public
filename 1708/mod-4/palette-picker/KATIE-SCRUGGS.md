# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/katiescruggs/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-scruggs.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/katiescruggs/palette-picker/blob/annotate-server/server.js)

## Completion

#### Were you able to complete the base functionality?
I think I was able to complete the vast majority of the base functionality. One thing I know is undone is that even though the server does not save two projects with the same title, the titles still append in the dropdown menu. I couldn't figure out how to fix that bug, but will work on it this weekend.

#### Which extensions, if any, did you complete?
No extensions completed. The text color of the hex code does change colors depending on the color selected, which I thought was pretty cool.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/katiescruggs/palette-picker/blob/268933e58f41555b3d37452030620028de82c2b1/test/routes.spec.js#L94-L120)

* Why were you proud of this piece of code?

I'm proud of this piece of code because it was challenging to get the proper projectId to post a palette to because the database is reseeding. I also actually really like testing and was able to make my server handlers better because of the testing that I was able to implement.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/katiescruggs/palette-picker/blob/268933e58f41555b3d37452030620028de82c2b1/test/routes.spec.js#L205-L233)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I was very sad that I could not get this test to pass. It was the last test I felt was necessary to completely test my back-end functionality. It was challenging in the tests to get the correct projectId and paletteId because of the constant re-seeding of the database. For this test, I got an error that was not super helpful to debugging, and I ran out of time to try to make it work.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()
Palette Picker running on 3000
  Client Routes
    ✓ should return the homepage
    ✓ should return a 404 for a route that does not exist

  API Routes
    GET /api/v1/projects
Seeding complete
      ✓ should return all of the projects
    POST /api/v1/projects
Seeding complete
[]
      ✓ should create a new project
Seeding complete
      ✓ should not create a record with missing data
    GET /api/v1/projects/:projectId/palettes
Seeding complete
      ✓ should return the palettes for one project
Seeding complete
      ✓ should return a 404 if the project is not found
    POST /api/v1/projects/:projectId/palettes
Seeding complete
      ✓ should create a palette
Seeding complete
      ✓ should return error if title parameter is missing
Seeding complete
      ✓ should return error if color1 parameter is missing
    DELETE /api/v1/projects/:projectId/palettes/:paletteId
      - should delete a palette


  10 passing (183ms)
  1 pending

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

For my main source of design inspiration, I used the website [coolors.co](https://coolors.co/). I really like the simplicity of the color blocks, how much of the screen they take up, using the spacebar to change the colors, and the sidebar for all of the controls. 

I also looked at several color palettes on dribbble, like [this one](https://cdn.dribbble.com/users/60174/screenshots/2684569/color_palette.png). I noticed during this research that the color palettes I enjoyed were very simple with no distractions of font or background colors, and I implemented these design concepts into my app by making the background colors gray and trying to make the hex code font as minimal yet easy to read as possible.

#### Please feel free to ask any other questions or make any other statements below!

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

