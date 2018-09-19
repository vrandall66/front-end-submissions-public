# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/tdberg21/byob)

#### Link to the Deployed Application
[Heroku](https://byodogparty.herokuapp.com/)


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

* Setup automatic deployments with TravisCI to a production app on Heroku?
(Yes)

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/tdberg21/byob/blob/88bb7528d8363e04728f50fbc0402b4137be27e9/server.js#L20)

* Why were you proud of this piece of code?
It was exciting getting the JWT authorization to work for the first time!

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/tdberg21/byob/blob/88bb7528d8363e04728f50fbc0402b4137be27e9/server.js#L194)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
We could get the patches to update the database as we wanted, but the response is still an error.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

THEY'RE GOOD DOGS BRENT is running on 3000
  Client Routes
    ✓ should return a home page
    ✓ should return a 404 for a route that does not exist

  API Routes
    GET /api/v1/groups
The seeds have been planted.
      ✓ should return all the groups
    GET /api/v1/groups/:id
The seeds have been planted.
      ✓ should return a specific group
The seeds have been planted.
{ error: 'Unable to find a breed group with the id: "236"' }
      ✓ should not return a 404 if a group does not exist
    GET /api/v1/breeds
The seeds have been planted.
      ✓ should return all the breeds
    GET /api/v1/breeds/:id
The seeds have been planted.
      ✓ should return a specific breed
The seeds have been planted.
      ✓ should not return a 404 if a breed does not exist
    POST /api/v1/groups
      - should create a new breed group
      - should return a 422 status code if breed group parameters are missing
    POST /api/v1/breeds
      - should create a new breed
      - should return a 422 status code if breed parameters are missing
    DELETE /api/v1/groups/:id
      - should delete a specific group from the database
The seeds have been planted.
      ✓ should return a 404 for a group that does not exist
    DELETE /api/v1/breeds/:id
The seeds have been planted.
      ✓ should delete a specific breed from the database
      - should return a 404 for a breed that does not exist
    PATCH /api/v1/groups/:id
      - should update a breed group record
      - should return a 422 for an incorrect request
    PATCH /api/v1/breeds/:id
      - should update a breed record
      - should return a 422 for an incorrect request


  10 passing (2s)
  10 pending

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

byob (prevals) ⛷  ▶ npm run eslint

> byob@1.0.0 eslint /Users/torydberg/Documents/Documents - Tory’s MacBook Pro/Turing/mod-4/projects/byob
> ./node_modules/eslint/bin/eslint.js *.js --ignore-pattern *.test.js

byob (prevals) ⛷  ▶

#### Attach a screenshot of your TravisCI build passing

[TravisCI build](https://travis-ci.org/tdberg21/byob/builds/424126925)

￼
-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you want to say?
They’re good dogs, Brent. 


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
