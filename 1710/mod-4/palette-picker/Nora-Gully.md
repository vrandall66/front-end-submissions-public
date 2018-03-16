# Palette Picker Submission

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/nogully/palette-picker)

#### Link to the Deployed Application
[heroku](https://swatch-saver.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/nogully/palette-picker/blob/commented-server-file/server.js)

## Completion

#### Were you able to complete the base functionality?

Yes

If not, explain what is missing and why.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/nogully/palette-picker/blob/1a10a1cf6b00e38c9cf7c9905c7ccb0aec1571bf/public/js/scripts.js#L27-L38)

* Why were you proud of this piece of code?
I liked using .toArray() with jQuery to create an array of elements to iterate through

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/nogully/palette-picker/blob/1a10a1cf6b00e38c9cf7c9905c7ccb0aec1571bf/public/js/scripts.js#L84-L107)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
I tried to use the server to check the database for a given project name and to generate an error if that name already existed, but I ran out of time to make that work.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```API Routes
    GET /api/v1/projects
      ✓ should return all of the projects
    GET /api/v1/projects/:id/palettes
      ✓ should return all of the palettes for a given project
      ✓ should return an error 404 if it can't find palettes for that project
    POST /api/v1/projects
      ✓ should create a new project
      ✓ should return status 422 if missing params in the body
    GET /api/v1/palettes
      ✓ should return all of the palettes
    POST /api/v1/palettes
      ✓ should create a new palette
      ✓ should return status 422 if missing params in the body
    GET /api/v1/palettes/:id
      ✓ should return the palette with given id
      ✓ should return an error 404 if it can't find a palette with that id
    DELETE /api/v1/palettes/:id
      ✓ should delete the palette with given id
      ✓ should return an error 404 if it can't find a palette with that id
  14 passing (1s)
```

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it
[palette image](https://goo.gl/images/BmP8qB) 
I used a wood grain background because I thought it evoked the idea of an artist's palette and paints. 

#### Please feel free to ask any other questions or make any other statements below!
I would have liked to have had more time to create better error handling and sad path cases. 

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
