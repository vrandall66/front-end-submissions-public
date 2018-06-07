# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/JSweet314/palette-picker)

#### Link to the Deployed Application
[heroku](https://palettepicker-js.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/JSweet314/palette-picker/blob/annotate/server.js)

## Completion

#### Were you able to complete the base functionality?

Yes.

#### Which extensions, if any, did you complete?

N/A

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of

[happy code](https://github.com/JSweet314/palette-picker/blob/b1cf1b03d79565fbfd7e5e4e010e54bfcd8e3921/public/js/PalettePicker.js#L11)

* Why were you proud of this piece of code?

I was able to take an OOP approach and incorporate asynchronous methods inside the PalettePicker class to store data from server to use in the application.

#### Link to a specific block of your code on GitHub that you feel not great about

[sad code](https://github.com/JSweet314/palette-picker/blob/b1cf1b03d79565fbfd7e5e4e010e54bfcd8e3921/public/js/index.js#L23)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

The functions that return template literals could probably be pulled out in to a seperate file containing just methods that return 'html'. A different approach might be possible to avoid making this function asynchronous as it has to await the response of the server to populate the constructor of the PalettePicker method with data from the server.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
Palette Picker server running on 3000.
  Color
    ✓ should have a hex color
    ✓ should be able to randomly generate a hex color
    ✓ should have a property locked, which can be toggled
    ✓ shoud be able to update its own color

  Palette
    ✓ should hold five Color instances in an array
    ✓ should be able to update only unlocked colors
    ✓ should be able to toggle a color lock by its index position

  Client Routes
    ✓ should serve up public html assets by default
    ✓ should return a 404 for an unknown route

  API Routes
    ✓ GET palettes should return all of the palettes
    ✓ GET projects should return all of the projects
    ✓ POST projcet should add a new project to the DB
    ✓ POST project should return status 422 with error message if missing a parameter
    ✓ POST palette should add a palette to the DB
    ✓ POST palette should return status 422 with an error message if missing a parameter
    ✓ DELETE palette should delete a palette from the DB
    ✓ DELETE palette should return status 422 with error message if missing a parameter


  17 passing (463ms)
```

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

[Dribbble example](https://dribbble.com/shots/352763-Sidebar-Stats-Full)

I like the organizational approach this design takes to the sidebar assets. I stole the layout idea and the hierarchy of fonts and adopted some of my own style relative to the needs of my app and a stauncher border to separate projects.

#### Please feel free to ask any other questions or make any other statements below!

Working with jQuery again wasn't as painful as I expected. It is a lot easier now for me to dive in to the documentation that it was in mod 1!

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

