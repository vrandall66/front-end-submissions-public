# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/t-laird/ufo-tracker)

#### Link to the Deployed Application
[Heroku](https://ufo-tracker-thawk.herokuapp.com/)


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
Yes

* Wrote tests for both happy and sad paths for each endpoint?
Yes

* Setup automatic deployments with CircleCI to a production app on Heroku?
Yes

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
Thomas - [happy code](https://github.com/t-laird/ufo-tracker/blob/f6fd0ae41ff1ba734a11c1295c379587449ba30a/db/seeds/dev/ufo-data.js#L16-L49)

Julie - [happy code](https://github.com/t-laird/ufo-tracker/blob/f6fd0ae41ff1ba734a11c1295c379587449ba30a/test/routes.spec.js#L114-L133)


* Why were you proud of this piece of code?

Thomas - We needed two relations given our 3 tables so we had to use two helpers to get our Location and Shape IDs. Since both of these functions were asynchronous we had to come up with a creative solution to return the data appropriately. Our solution - using a nested series of promises that are all wrapped in a Promise.all, while not the cleanest, solves this complex problem effectively and preserves the integrity of the informating being seeded in.

Julie - Using .every here allowed us to avoid testing all of the objects returned in the response individually and makes this test cover the server response more fully.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/t-laird/ufo-tracker/blob/dd6d8343c2eae3fa0425009daa2b8f53b11e1885/server.js#L97-L105)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

We would have liked to refactor this code and the other helper function into one function that could be reused in all cases where a helper is necessary.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

![test suite](https://github.com/t-laird/ufo-tracker/blob/master/byob-tests.png?raw=true)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

![linter output](https://github.com/t-laird/ufo-tracker/blob/master/byob-eslint.png?raw=true)

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://circleci.com/gh/t-laird/ufo-tracker/17)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say

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
