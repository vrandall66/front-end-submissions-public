# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/airum82/Palette-town)

#### Link to the Deployed Application
[heroku](https://palette-town.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/airum82/Palette-town/blob/master/server.js)

## Completion

#### Were you able to complete the base functionality?

In general yes, the one part I did not get to was the dribble inspiration because I did not allocate time for it.

#### Which extensions, if any, did you complete? None

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/airum82/Palette-town/blob/master/server.js#L33-L43)

It was my first express function that used a dynamic endpoint and it also saved my palettes.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/airum82/Palette-town/blob/master/public/js/scripts.js#L165-L188)

This function was big and the jquery path I used for appending the palettes was convoluted. Also I did not get to refactoring it.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

Palette town running on localhost:3000

  GET /api/v1/folders
  
    ✓ should return an array of projects
    
    ✓ should return 500 error if fetch fails

  GET /api/v1/palettes
  
    ✓ should return an array of palettes

  PUT/POST/DELETE
  
    ✓ should insert a new folder into database
    
    ✓ /api/v1/newFolder should create a new folder in database
    
    ✓ api/v1/newFolder should return error if no project name
    
    ✓ /api/v1/delete/palette

  7 passing (700ms)

#### Link to Design Inspiration

I decided to have the style be similar to that of the pokemon games so I used a picture of palette town from one of the games and used styling that would go with the background image.

https://github.com/airum82/Palette-town/blob/master/public/Kanto_Pallet_Town_Map.png

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
