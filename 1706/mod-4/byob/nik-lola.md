# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/NikBorn/byob)

#### Link to the Deployed Application
[Heroku](https://boyb-byob.herokuapp.com/)


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
[happy code](https://github.com/NikBorn/byob/blob/master/server.js#L29-L56)

* Why were you proud of this piece of code?

It handles the testing env as well as authentication and authorization in one function.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/NikBorn/byob/blob/master/test/routes.spec.js#L144-L151)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
We were not getting an error message back when testing this sad path, so we took out the validation for it so the test would pass.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()
Test Seeding Complete!
      ✓ should not be able to update a bill record if the user is trying to change the id
    PATCH /api/v1/houses/:houseId/chores/:id
Test Seeding Complete!
      ✓ should be able to update a chore record
Test Seeding Complete!
      ✓ should not be able to update a bill record if the record does not exist
Test Seeding Complete!
      ✓ should not be able to update a chore record if the user is trying to change the id
    PATCH /api/v1/houses/:houseId/bulletins/:id
Test Seeding Complete!
      ✓ should be able to update a bulletin record
Test Seeding Complete!
      ✓ should not be able to update a bulletin record if the record does not exist
Test Seeding Complete!
      ✓ should not be able to update a bulletin record if the user is trying to change the id
    DELETE /api/v1/houses/:houseId/bills/:id
Test Seeding Complete!
      ✓ should delete bill with id specified
Test Seeding Complete!
      ✓ should return 422 if no bill found
    DELETE /api/v1/houses/:houseId/chores/:id
Test Seeding Complete!
      ✓ should delete chore with id specified
Test Seeding Complete!
      ✓ should return 422 if no chore found
    DELETE /api/v1/houses/:houseId/bulletins/:id
Test Seeding Complete!
      ✓ should delete bulletin with id specified
Test Seeding Complete!
      ✓ should return 422 if no bulletin found


  52 passing (4s)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output]()

Lolas-Koala-Sparkle-Machine:byob lolakoala$ npm run lint

> byob@1.0.0 lint /Users/amandabrenner/turing/mod4/byob
> eslint ./

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://github.com/NikBorn/byob/blob/master/assests/Screen%20Shot%202017-12-15%20at%2012.44.35%20PM.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say


-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**x points**:(10 possible points) Lorem ipsum dolor set amet

### Feature Completion

**x points**: (60 possible points) Lorem ipsum dolor set amet

### Testing & Linting & Error Handling

**x points**: (40 possible points) Lorem ipsum dolor set amet

### JavaScript Style

**x points**: (40 possible points) Lorem ipsum dolor set amet

### Workflow

**x points**: (20 possible points) Lorem ipsum dolor set amet

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: x / 170
