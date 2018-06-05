# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/skenne21/BYOB)

#### Link to the Deployed Application
[Heroku](https://skenne21.herokuapp.com/)


## Completion

#### Were you able to complete the base functionality? Yes

* Documented all available endpoints and their usage in the README?
(Yes)

* Seeded a database with at least 2 tables and 1 relationship?
(Yes

* Had at least 10 endpoints that returned responses with appropriate status codes?
(Yes

* Secured at least 4 endpoints with JWTs?
(Yes

* Enforced a linter and wrote code that conformed to it?
(Yes

* Wrote tests for both happy and sad paths for each endpoint?
(Yes

* Setup automatic deployments with TravisCI to a production app on Heroku?
(Yes

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/skenne21/BYOB/blob/8738bc7f50791b9720f6e786f17d3e0b120a09c0/scraping-data/parksNightmare.js#L1-L40)

We are proud of being able to figure out how to use nightmare and pull in the data clean and seed to database. 

* Why were you proud of this piece of code?

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/skenne21/BYOB/blob/8738bc7f50791b9720f6e786f17d3e0b120a09c0/server.js#L28-L60)

For the admin web token and the normal user token we were not sure if we went the right way with our methods, and wanted to refactor to one method but never were able to make it work. 

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

parkFinder is running on port 3000
  client-routes
    ✓ should return homepage with an html document
    ✓ should return 404 if the request is not found

  API-routes
    GET /api/v1/states
      ✓ should get all the states
      ✓ should get a state with an abbv
      ✓ should send a 422 status if the state Abbv does not exist
    GET /api/v1/parks
      ✓ gets all the parks
    GET /api/v1/states/:id
      ✓ gets a state by id
      ✓ should send a status of 404 if id does not exist
    GET /api/v1/parks/:id
      ✓ should return a park by id
      ✓ should send a status of 404 if id does not exist
    GET /api/v1/states/:id/parks
      ✓ should return an array of all parks with a specific state id
      ✓ should send a status of 404 if id does not exist
    POST /api/v1/states
      ✓ should post a new new state to the database
      ✓ should send 422 if missing req params
    POST /api/v1/parks
      ✓ should post a new park to the database
      ✓ should send 422 if missing req params
    DELETE /api/v1/states/:id
      ✓ should delete a record with a spec id
      ✓ should send a status of 404 if the id does not match
    DELETE /api/v1/parks/:id
      ✓ should delete a record with a spec id
      ✓ should send a status of 404 if the id does not match
    PUT /api/v1/states/:id
      ✓ should modify a single state by id
      ✓ should send 422 if missing req params
    PUT /api/v1/parks/:id
      ✓ should replace a single park by id
      ✓ should send 422 if missing req params


  24 passing (2s)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output]()

npm run eslint

> BYOB@1.0.0 eslint /Users/stevenlawson/Turing/mod4/projects/BYOB
> ./node_modules/eslint/bin/eslint.js ./


/Users/stevenlawson/Turing/mod4/projects/BYOB/public/scripts/script.js
 4:30  error  Parsing error: Unexpected token =>

:heavy_multiplication_x: 1 problem (1 error, 0 warnings)

#### Attach a screenshot of your TravisCI build passing

[TravisCI build]()

 BYOB@1.0.0 test /home/travis/build/skenne21/BYOB
> NODE_ENV=test mocha --exit
parkFinder is running on port 3000
  client-routes
    ✓ should return homepage with an html document
    ✓ should return 404 if the request is not found
  API-routes
    GET /api/v1/states
      ✓ should get all the states
      ✓ should get a state with an abbv
      ✓ should send a 422 status if the state Abbv does not exist
    GET /api/v1/parks
      ✓ gets all the parks
    GET /api/v1/states/:id
      ✓ gets a state by id
      ✓ should send a status of 404 if id does not exist
    GET /api/v1/parks/:id
      ✓ should return a park by id
      ✓ should send a status of 404 if id does not exist
    GET /api/v1/states/:id/parks
      1) should return an array of all parks with a specific state id
      ✓ should send a status of 404 if id does not exist
    POST /api/v1/states
      ✓ should post a new new state to the database
      ✓ should send 422 if missing req params
    POST /api/v1/parks
      ✓ should post a new park to the database
      ✓ should send 422 if missing req params
    DELETE /api/v1/states/:id
      ✓ should delete a record with a spec id
      ✓ should send a status of 404 if the id does not match
    DELETE /api/v1/parks/:id
      ✓ should delete a record with a spec id
      ✓ should send a status of 404 if the id does not match
    PUT /api/v1/states/:id
      ✓ should modify a single state by id
      ✓ should send 422 if missing req params
    PUT /api/v1/parks/:id
      ✓ should replace a single park by id
      ✓ should send 422 if missing req params
  23 passing (3s)
  1 failing
We cant get travis to pass this one test, but it passes local everytime. we think the issue is the before each and seeding the test database, but cant figure out how to solve the issue without skipped test and we did not want a skipped test in our repo that is passsing.

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you want to say?

-----


# Instructor Feedback (Instructor Name)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**x points**: (10 possible points)

### Feature Completion

**x points**: (60 possible points)

### Testing & Linting & Error Handling

**x points**: (40 possible points)

### JavaScript Style

**x points**: (40 possible points)

### Workflow

**x points**: (20 possible points)

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: x / 170
