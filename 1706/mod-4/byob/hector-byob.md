# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/hsanchez7934/hs-build-your-own-backend)

#### Link to the Deployed Application
[Heroku](https://hs-byob-12-17-2017.herokuapp.com/)


## Completion

#### Were you able to complete the base functionality?

* Documented all available endpoints and their usage in the README?
(Yes)

* Seeded a database with at least 2 tables and 1 relationship?
(Yes)

* Had at least 10 endpoints that returned responses with appropriate status codes?
(Yes)

* Secured at least 4 endpoints with JWTs?
(Yes)

* Enforced a linter and wrote code that conformed to it?
(Yes)

* Wrote tests for both happy and sad paths for each endpoint?
(Yes)

* Setup automatic deployments with CircleCI to a production app on Heroku?
(Yes)

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of

[happy code](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/db/seeds/dev/watches.js)
Lines 4 through 25; functions createBrands and createWatch.

* Why were you proud of this piece of code?
Took me a while to figure out how to seed the large data set that I'm using.
The first few functions that I wrote were long and sloppy but in the end I was able to end up with a few lines
of code and the functions work the way I want them to.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/test/routes.spec.js)
Lines 220 through 251

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
  These test have been problematic. I've had issues trying to debug them.  The test that begins on 220 passes when I run npm 
  test, but when circle ci starts the build process, it fails.  The second test will not pass, the only error I get
  is that I need to ensure that I call done.  I need to refactor and debug so I can fix these issues.
  
  
#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

BYOB is running on 3002.
  Client Routes
    ✓ should return the homepage with text (70ms)
    ✓ should return 404 error for nonexistent route

  API Routes
    ✓ should return a token for a user,
      if email ends in turing.io user.admin
      property should be set to true
    ✓ should return a token for a user,
      if email does not end in turing.io user.admin
      property should be set to false
    ✓ should retrieve all brands

express deprecated req.param(name): Use req.params, req.body, or req.query instead server.js:83:23
express deprecated req.param(name): Use req.params, req.body, or req.query instead server.js:84:23
    ✓ should retrieve all watch models
    ✓ should retrieve all watch models that
           match min and max parameter requirements,
           this test has a min of 0 and max of 3000
           for price range
    ✓ should return status 404 if no watches match
      the min and max parameter requirements,
      for this test the min is 0 and max is 10
    ✓ should retrieve specific brand by id number
    ✓ should retrieve specific watch by id number
    ✓ should retrieve all watch models by brand, using brand id
    ✓ should be able to post a new brand
      to watch_brands database
    - should not be able to post a new
      brand when user is not authorized
    ✓ should be able to post a new watch
      to watch_brands database
    ✓ should be able to update an existing brand
    ✓ should be able to delete brand by id
    (node:85877) UnhandledPromiseRejectionWarning: Unhandled promise rejection (rejection id: 1): Error: Internal Server Error
    ✓ should be able to delete watch by id

  17 passing (778ms)
  1 pending

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

Hector:byob hector$ npm run lint

> byob@1.0.0 lint /Users/hector/byob
> eslint ./

Hector:byob hector$

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/assets/circleci.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say

-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**7 points**: The README includes documentation for all available endpoints and how to use them. Instructor can mostly follow the documentation for using the API.

* There is very little formatting in the README which makes it a bit difficult to read, in some areas the heading formats aren't being parsed correctly. (The BYOB title for example)

* Generally you don't want to include images as part of your documentation for code...it's nice for people to be able to do a cmd+F to search for some text they're looking for. When you use images, it's impossible to do that.

* Glad you put in request body examples for your POST and PATCH requests, but I'd like you to be a little more explicit about what data type each property must be. I can infer based on the strings in the example, but it'd be nice to explicitly tell the user that.

### Feature Completion

**x points**: (60 possible points) Lorem ipsum dolor set amet

### Testing & Linting & Error Handling

**x points**: (40 possible points) Lorem ipsum dolor set amet

### JavaScript Style

**x points**: (40 possible points) Lorem ipsum dolor set amet

### Workflow

**x points**: (20 possible points) Lorem ipsum dolor set amet

* [This](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/.DS_Store) should be in your .gitignore file

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: x / 170
