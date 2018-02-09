# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/jasonhughes1/BYOB)

#### Link to the Deployed Application
[Heroku](http://byob-jk.herokuapp.com/)


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
No - CircleCI is not seeding our test database properly, so 4 of our tests are failing in CircleCI even though they pass locally.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/jasonhughes1/BYOB/blob/master/test/routes.spec.js)

* Why were you proud of this piece of code?
We're proud of how we testing our program with happy and sad paths for each endpoint!

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/jasonhughes1/BYOB/blob/master/circle.yml)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
This file gave us so much trouble, and as of this writing we still haven't gotten CircleCI to run our tests properly.
Hopefully we will get it to work sometime soon.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite 1](https://github.com/jasonhughes1/BYOB/blob/master/test1.png)
[test suite 2](https://github.com/jasonhughes1/BYOB/blob/master/test2.png)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](https://github.com/jasonhughes1/BYOB/blob/master/eslint.png)

#### Attach a screenshot of your CircleCI build passing

[circleCI build]() not passing

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say

-----


# Instructor Feedback (Instructor Name)

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
