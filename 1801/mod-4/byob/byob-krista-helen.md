# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/hdechat/byob-volcanoes)

#### Link to the Deployed Application
[Heroku](https://byob-volcanoes-krishel.herokuapp.com/)


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

* Setup automatic deployments with TravisCI to a production app on Heroku?
Yes

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/hdechat/byob-volcanoes/blob/77c8a4c227aa96a228031afb4366d9bb3d9cc36a/test/routes.spec.js#L189-L225)

* Why were you proud of this piece of code?  
We were proud of this code because we struggled with testing some endpoints other than `GET` endpoints due to certain information being different each time. We were able to figure out how to avoid this issue by rolling back our seeded data in the beforeEach hook.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/hdechat/byob-volcanoes/blob/77c8a4c227aa96a228031afb4366d9bb3d9cc36a/server.js#L215-L231)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?  
We were certain that there was a better way to check the requested keys against the data stored in the database. We did not have time to refactor this.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://user-images.githubusercontent.com/11744547/42718589-852c974c-86c7-11e8-8245-3fbbebd5eec9.png)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](https://user-images.githubusercontent.com/11744547/42718559-39697f6e-86c7-11e8-9eeb-2cf8eac63757.png)

#### Attach a screenshot of your TravisCI build passing

[TravisCI build](https://user-images.githubusercontent.com/11744547/42720986-37970efe-86ef-11e8-91fd-9587c986f303.png)

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