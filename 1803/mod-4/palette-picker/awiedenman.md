# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/Awiedenman/palette-picker)

#### Link to the Deployed Application
[heroku](https://austins-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/Awiedenman/palette-picker/blob/master/server.js#L1-L179)

## Completion

#### Were you able to complete the base functionality?

I encountered a few bugs with saving my palettes into the correct folder. Once refreshed everything comes out correctly.

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/Awiedenman/palette-picker/blob/master/server.js#L161)

* Why were you proud of this piece of code?
I felt really proud of creating the backend and understanding it more.  I built out a postgres backend for my mod3 personal project, but I had very little understanding of how things actually worked. Being able to create databases open up a lot more opportunities to build out and store meaningful data.  I was also having a bunch of weird errors in my test suite that I am still working to fix.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/Awiedenman/palette-picker/blob/master/public/script.js#L130-L148)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?  
This functionality was working previously and I broke it through fixing other bugs.  I need to reassign the id to the projects when they are created and then check to see if the text in the drop down menu matches when I create a palette.  Create conditional that checks if teh project exists, if so append there, if not, create new project.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

alette Picker is running on 3000.
  api routes
    GET api/v1/projects
Seeding complete!
      ✓ should return all projects
    GET api/v1/palettes/:id
Seeding complete!
      ✓ should return a single palette
Seeding complete!
      ✓ should return an error if id doesn't exist
    GET api/v1/projects/:project_name
Seeding complete!
      ✓ should return a single project
Seeding complete!
      ✓ should return an error if project_name doesn't exist
    DELETE api/v1/palettes/:palette_id
Seeding complete!
      ✓ should delete a single palette
    POST /api/v1/projects/
Seeding complete!
      ✓ should post a single project
    POST /api/v1/palettes/
Seeding complete!
      ✓ should post a single palette
Seeding complete!
      ✓ should return an error if palette cant post


  9 passing (649ms)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it
[coolers](https://coolors.co/495867-577399-bdd5ea-f7f7ff-fe5f55)
I took most of my styling inspiration from the spec and from coolers.
[colour-palettes](https://dribbble.com/shots/891640-Colour-Palettes)
I got teh idea for my logo from this dribble.
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
