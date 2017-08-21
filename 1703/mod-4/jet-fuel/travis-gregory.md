# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/tlgreg86/jet-fuel)

#### Link to the Deployed Application
[heroku](https://tg-jetfuel.herokuapp.com/)

#### Link to your annotated server file
[annotated server file]()
* I ran out of time and didn't get to annotate my server file.

## Completion

#### Were you able to complete the base functionality?

I wasn't able to get to the point of sorting the data and I didn't get the urls add date formatted the way I wanted because I just had a difficult time getting through testing and getting the routes and backend hooked up. Those are the only pieces I wasn't able to complete, that I know of at least.

#### Which extensions, if any, did you complete?

I didn't get far enough to do any of the extentions.

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/tlgreg86/jet-fuel/blob/8dbf6f42f06cfec1e8a972b411e959a5ffc60852/server.js#L30)

* This part just took me a while to get working correctly and it felt good to get it down.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/tlgreg86/jet-fuel/blob/8dbf6f42f06cfec1e8a972b411e959a5ffc60852/public/scripts.js#L134)

* This code is just really ugly and I found it to be difficult just dealing with all of the conditionals involved with the regex.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]

travis: jet-fuel (master) >> npm test

> jet-fuel@1.0.0 test /Users/travis/Documents/Turing/4-Mod/projects/jet-fuel
> mocha

Jet Fuel is running on http://localhost:3000.
  Client routes
    ✓ should return the homepage (46ms)
    ✓ should return error 404 if route does not exist

  API Routes
    GET /api/v1/folders gets all folders
      ✓ should return an array of folders
    POST /api/v1/folders adds to folders
      ✓ should create a new folder
      ✓ should not create a folder if a parameter is missing
    GET /api/v1/folders/:id/urls
      ✓ should return all urls
    POST /api/v1/folders/:id/urls
      ✓ should create a new url
      ✓ should not create a url with missing parameters
    GET /api/v1/urls/:id
      - should return the original url


  8 passing (299ms)
  1 pending

#### Please feel free to ask any other questions or make any other statements below!

This project was really difficult for me and though I got through most of it I did not get so far as to comment out my server file. I would still like to do it if I'm allowed.

-----


# Instructor Feedback (Instructor Name)

## Specification Adherence

**x points**: Lorem ipsum dolor set amet

## User Interface

**x points**: Lorem ipsum dolor set amet

## Data Persistence with SQL Database

**x points**: Lorem ipsum dolor set amet

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**x points**: Lorem ipsum dolor set amet


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: x / 150
