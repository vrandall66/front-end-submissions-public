# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/francylang/byob)

#### Link to the Deployed Application
[Heroku](https://speed-running-database.herokuapp.com/)


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
Yes. Missing testing on some delete sad paths and authorization testing. 

* Setup automatic deployments with CircleCI to a production app on Heroku?
Circle CI build failed due to test suite.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/francylang/byob/blob/master/db/migrations/20171212142017_initial.js#L11)

* Why were you proud of this piece of code?

We had originally wanted to create a many to many relationship, as a game could have many speedrunners and a speedrunner could have records for many games. Building the schema for a one to many relationship proved to be easier, and were proud of our implementation to simplify the relationship without using a joined table. 

We were also pretty excited about getting githooks into our project.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/francylang/byob/blob/master/test/routes.spec.js#L65)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

While applying `done()` to our testing suites, we ran into frustrating inconsistencies. Sometimes the tests would fail and throw errors about `done()`, and without changing anything the next time the tests ran everything would be fine. These inconsistencies would happen when we included the `done()` as well as when we removed it. This is our sad code because we were unable to properly debug the issue and couldn't find a reason for the errors. 

This inconsistency would make our Circle CI build fail - tests would be passing locally but not on the build. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://github.com/francylang/byob/blob/master/test/routes.spec.js)
<img width="512" alt="screen_shot_2017-12-15_at_9 06 58_am_1024" src="https://user-images.githubusercontent.com/26471447/34050764-426175e8-e179-11e7-8e11-1b15a34ccdfe.png">


#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](https://github.com/francylang/byob/blob/master/.eslintrc.js)
<img width="570" alt="screen shot 2017-12-15 at 9 17 00 am" src="https://user-images.githubusercontent.com/26471447/34050709-09b780fc-e179-11e7-971a-9d632a5d0238.png">


#### Attach a screenshot of your CircleCI build passing

[circleCI build]()


-----

#### Please feel free to ask any other questions or make any other statements below!

We were unable to remove warnings about unhandled promise rejections in our test suite. We were unable to resolve this warning.
```
GET /api/v1/records/:id
(node:93162) UnhandledPromiseRejectionWarning: Unhandled promise rejection (rejection id: 1): AssertionError: expected 0 to equal 1
(node:93162) [DEP0018] DeprecationWarning: Unhandled promise rejections are deprecated. In the future, promise rejections that are not handled will terminate the Node.js process with a non-zero exit code.
```

While we were able to setup our Heroku and Circle CI for this project, the inconsistent test suite stopped us from creating a passing build. Our application on Heroku is working fine. 

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
