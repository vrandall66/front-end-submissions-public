# Palette Picker Submission Form - James Logue

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/jjlljj/palette-picker)

#### Link to the Deployed Application
[heroku](https://palettepickerjl.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/jjlljj/palette-picker/blob/server-file-comments/server.js)

## Completion

#### Were you able to complete the base functionality?

I was able to complete all of the base functionality.

#### Which extensions, if any, did you complete?

No extensions, though I would have liked to make the colors user selectable.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/jjlljj/palette-picker/blob/e6038557185d87c3764fac6719c5eb49fbd3ea7e/public/scripts/scripts.js#L76)

* I am happy that I was able to do all of my rendering and display functions entirely in vanilla JS. Previously I would have used jQuery to this, as it has a couple of methods which explicitly make it easy to append/prepend, but I wanted to challenge myself by using vanilla JS, and it ended up being very doable. 

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code endpoint](https://github.com/jjlljj/palette-picker/blob/75abcb8b4ce05aaf9e723a917b4997a601a0bb1a/server.js#L86)

* This endpoint and the fetch that calls it are both too complicated. I wrote them initially to handle  data being passed to app.locals, so when I moved over to the db, I ended up having to do cleaning in my endpoint code based on what I was passing in the fetch request, because of the discrepancy between camelCase front end data names, and snake_case db data. I intended to refactor it, but didn't get to because it would mean tracking down the everywhere i've passed that response around in the FE.


* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()

  Client Routes
    ✓ should return the homepage
    ✓ should return 404 for page that does exist

  API Routes
    GET /api/v1/projects
      ✓ should return all of the projects
    POST /api/v1/projects
      ✓ should create a new project (40ms)
      ✓ should return 422 if missing information in the body
    GET /api/v1/palettes
      ✓ should return all of the palettes
    GET /api/v1/palettes/:id
      ✓ should return the expected palette
      ✓ should return 404 if the palette is not found
    DELETE /api/v1/palettes/:id
      ✓ should delete the palette as expected
      ✓ should return 404 if there is no record to delete
    POST /api/v1/:id/palettes
      ✓ should add the project palette to the db
      ✓ should return 422 if missing expected params


  12 passing (1s)

#### Link to Design Inspiration

* I really liked and wanted to implement the color shifing that Coolers does with their text superimposed over the color, where it is a lighter, semi-tranparent font color when the color is dark, and darker when the color is light. I didn't have time to figure out how to detect the color tone based on hex, so I kind of mocked this interaction with a lighter, semi-transparent font color and a hover state for the darker font color.

* I also like the rounded menu's and forms that you see on websites like indeed, so I implemented a version of that for my forms.

#### Please feel free to ask any other questions or make any other statements below!

This project was fun, and it mades me really appreciate React because it was a big adjustment going back to writing regular HTML. I am excited that I was able to build it all in Vanilla, and it made me realize how far I've come in being able to use JS effectively.

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

