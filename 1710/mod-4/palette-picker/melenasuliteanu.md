# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/farmermel/palett-picker)

#### Link to the Deployed Application
[heroku](https://melenasuliteanu-palette-lab.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/farmermel/palett-picker/tree/commented)

## Completion

#### Were you able to complete the base functionality?

Yes!

#### Which extensions, if any, did you complete?

None

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/farmermel/palett-picker/blob/master/public/js/scripts.js#L170-L178)

* Why were you proud of this piece of code?

I like that all of the functions it uses are reusable and are used multiple times to access database and display retrieved items.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/farmermel/palett-picker/blob/master/public/js/scripts.js#L156-L168)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I don't like how it calls a bunch of other functions, all of which have loops to make a joined map of an array for each project and each palette. I think it could be more modular by individually appending things so that way the code can be reused when projects or palettes are added.


#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

``` Client Routes
    ✓ returns html homepage with appropriate elements
    ✓ returns 404 status for a route that does not exist
1

  API Routes
    GET /api/v1/palettes
Seeding complete!
      ✓ returns all of the projects
Seeding complete!
      ✓ returns a 404 status if endpoint does not exist
    POST /api/v1/palettes
Seeding complete!
      ✓ creates a new palette
Seeding complete!
      ✓ does not create a palette with missing data
    GET /api/v1/projects
Seeding complete!
      ✓ returns all of the projects
Seeding complete!
      ✓ returns a 404 status if endpoint does not exist
    GET /api/v1/projects/1
Seeding complete!
      ✓ returns project with requested id
Seeding complete!
      ✓ returns a 404 status if id does not exist
    POST /api/v1/projects
Seeding complete!
      ✓ creates a new project
Seeding complete!
      ✓ does not create a record with missing data


  12 passing (565ms)
```

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

[This icon exercise](https://dribbble.com/shots/4351747-Icon-Design-Exercise)
I like the use of white space, clean thin lines, and accents of pink. I tried to use this to inform my general design.

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

