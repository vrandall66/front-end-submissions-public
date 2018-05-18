# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/jaredeklin/byob)

#### Link to the Deployed Application
[Heroku](https://byob-jared-michael.herokuapp.com/)


## Completion

#### Were you able to complete the base functionality?

* Documented all available endpoints and their usage in the README? --YES

* Seeded a database with at least 2 tables and 1 relationship? --YES

* Had at least 10 endpoints that returned responses with appropriate status codes? --YES

* Secured at least 4 endpoints with JWTs? --YES

* Enforced a linter and wrote code that conformed to it? --YES

* Wrote tests for both happy and sad paths for each endpoint? --YES

* Setup automatic deployments with TravisCI to a production app on Heroku? --YES

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/jaredeklin/byob/blob/ce823a8a09efa602ef1f14307b0ef9d96e42d7db/public/js/index.js#L37)

We added the additional security measure of displaying the granted token in an alert.  This will encourage users to write their token down, as there is no copy/paste capability.  User further encourage to take great care of their token by indicating that replacement tokens will not be granted.  As the developer, we know this isn't completely truthful, but justifiable in the name of token security.  Finally, the use of the word 'Cred' (in three places) gives us street cred.

* Why were you proud of this piece of code?

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/jaredeklin/byob/blob/1d77eb3f0c984af3c4c6271b07762fc9e6721d0c/test/routes.spec.js#L36-L54)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

Our database does not seed in a consistent manner.  Artist with ID #30 currently may have a different ID the next time the test database is seeded.  Consequently, we were unable to reliably test the values of the properties.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://raw.githubusercontent.com/jaredeklin/byob/master/test/test-output.png)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](https://raw.githubusercontent.com/jaredeklin/byob/master/test/eslint-output.png)

#### Attach a screenshot of your TravisCI build passing

[TravisCI build](https://raw.githubusercontent.com/jaredeklin/byob/master/test/travis-output.png)

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
