# BYOB Submission Form

> Nick Svetnicka & Jason Lucas

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

## Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/EndlessHypnosis/build-your-own-backend)

#### Link to the Deployed Application
[Heroku](https://build-your-own-backend-brewery.herokuapp.com/)

#### Link to latest build on Circle CI
[Circle CI](https://circleci.com/gh/EndlessHypnosis/build-your-own-backend/57)

## Completion

#### Were you able to complete the base functionality?

* Documented all available endpoints and their usage in the README?

> YES

* Seeded a database with at least 2 tables and 1 relationship?

> YES

* Had at least 10 endpoints that returned responses with appropriate status codes?

> YES

* Secured at least 4 endpoints with JWTs?

> YES

* Enforced a linter and wrote code that conformed to it?

> YES

* Wrote tests for both happy and sad paths for each endpoint?

> YES

* Setup automatic deployments with CircleCI to a production app on Heroku?

> YES

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/EndlessHypnosis/build-your-own-backend/blob/master/server.js#L304-L333)

> This is the PUT endpoint for breweries. There's nothing terribly special about it, but we were proud of the fact that all edge cases were accounted for. The error checking is very complete and sanitizes the input for completeness before updating the record. We also made sure to delete the jwt token before sending the record to postgreSQL to update.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/EndlessHypnosis/build-your-own-backend/blob/master/server.js#L221-L236)

> We discussed the fact that both of our DELETE endpoints could be refactored to use one common function for handling the request validation, the knex delete, and finally building the response. The challenge we ran into was that this refactor should really entail the refactoring of all common endpoints with this approach, which we couldn't find the time for.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://github.com/EndlessHypnosis/build-your-own-backend/blob/master/public/assets/ss_testing.png)

![test suite](https://raw.githubusercontent.com/EndlessHypnosis/build-your-own-backend/master/public/assets/ss_testing.png)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](https://github.com/EndlessHypnosis/build-your-own-backend/blob/master/public/assets/ss_linter.png)

![eslint](https://raw.githubusercontent.com/EndlessHypnosis/build-your-own-backend/master/public/assets/ss_linter.png)

#### Attach a screenshot of your CircleCI build passing

[circleCI build](http://github.com/EndlessHypnosis/build-your-own-backend/blob/master/public/assets/ss_circle_ci.png)

![circle ci](https://raw.githubusercontent.com/EndlessHypnosis/build-your-own-backend/master/public/assets/ss_circle_ci.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

> N/A

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
