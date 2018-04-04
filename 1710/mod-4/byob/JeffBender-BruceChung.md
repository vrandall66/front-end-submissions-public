# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/brucekchung/byob)

#### Link to the Deployed Application
[Heroku](https://strengths-finder-be.herokuapp.com/)


## Completion

#### Were you able to complete the base functionality?

* Documented all available endpoints and their usage in the README?
Yes

* Seeded a database with at least 2 tables and 1 relationship?
Yes

* Had at least 10 endpoints that returned responses with appropriate status codes?
Yes

* Secured at least 4 endpoints with JWTs?
Yes

* Enforced a linter and wrote code that conformed to it?
No

* Wrote tests for both happy and sad paths for each endpoint?
Yes

* Setup automatic deployments with CircleCI to a production app on Heroku?
Yes

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/brucekchung/byob/blob/master/public/script.js)

* Why were you proud of this piece of code?
We were pretty happy to get the jwt working. It always great to be able to implement newly learned knowledge.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/brucekchung/byob/blob/master/strength-themes-data.js)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
We wanted to be able to have an array of complements per strength, but we're not sure how to set an array up w the schema.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
App is running on 3000
  API Routes
    GET /api/v1/strengths
      ✓ should have a GET route for strengths
      ✓ GET route for strengths should have optional query param complement
      ✓ should have a GET route for strengths by id
      ✓ should NOT GET route for STRENGTH with INVALID ID
    GET /api/v1/people
      ✓ should have a GET route for people
      ✓ should have a GET route for people by id
      ✓ should NOT GET route for PEOPLE with INVALID ID
    POST /api/v1/people
      ✓ Should add a new person
      ✓ Should NOT add a new person if NAME MISSING
    POST /api/v1/people/:people_id/strengths
      ✓ Should add a new strength to person
      ✓ Should NOT add a new person with missing strength
    DELETE /api/v1/people/:id
      ✓ Should delete a people by id
      ✓ Should NOT delete a people if id doesn't exist
    DELETE /api/v1/strengths/:id
      ✓ Should delete a strengths by id
      ✓ Should NOT delete a strengths if id doesn't exist
    PATCH /api/v1/people/:id
      ✓ Should patch people by id
      ✓ Should NOT patch people with INVALID ID
    PATCH /api/v1/strengths/:id
      ✓ Should patch strengths by id
      ✓ Should NOT patch strengths with INVALID ID


  19 passing (1s)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.
N/A

#### Attach a screenshot of your CircleCI build passing

![Travis CI Build](https://i.imgur.com/rbYhFzV.png)
![Travis CI Build](https://i.imgur.com/w08MJnE.png)

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
