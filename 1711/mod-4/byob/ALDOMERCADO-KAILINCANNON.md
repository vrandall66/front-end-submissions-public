# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/Kc2693/BYOB)

#### Link to the Deployed Application
[Heroku](https://byob-1711.herokuapp.com/)


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
[happy code](https://github.com/Kc2693/BYOB/blob/5f9f88e174ea721fb70cf1085be41d8cbeedbe47/server.js#L24-L36)

* Why were you proud of this piece of code?
Because it was the first time using a query selector in projects.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/Kc2693/BYOB/blob/5f9f88e174ea721fb70cf1085be41d8cbeedbe47/.travis.yml#L10-L14)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
Because it was late at night & it took us a long time to get TravisCI to deploy our heroku app.


#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
  Client Routes
    ✓ should return the home page (42ms)
    ✓ should return a 404 for a route that does not exist
  API Routes
Seeding complete
    ✓ GET muscle groups should return all the muscle groups
Seeding complete
    ✓ GET exercises should return all the exercises
Seeding complete
    ✓ GET exercises with query of level should exercises with level
Seeding complete
    ✓ GET muscle groups by id should return a single muscle group
Seeding complete
    ✓ GET muscle groups by id should return an error if no id in db
Seeding complete
    ✓ GET exercises by id should return a single exercise
Seeding complete
    ✓ GET exercises by id should return an error if no id in db
Seeding complete
    ✓ POST exercises should create a new exercise
Seeding complete
    ✓ POST exercises should not create an exercise w/ missing data 
Seeding complete
    ✓ POST muscle_groups should create a new muscle group
Seeding complete
    ✓ POST muscle grp will not create muscle grp w/ missing data 
Seeding complete
    ✓ POST authenticate should return a token
Seeding complete
    ✓ POST authenticate should not return a token if missing data
Seeding complete
    ✓ Patch exercises should update an exercise
Seeding complete
    ✓ Patch muscle groups should update a muscle group
Seeding complete
    ✓ DELETE exercise should remove an exercise from database
Seeding complete
    ✓ DELETE exercise should not remove an exercise w/ missing data
Seeding complete
    ✓ DELETE muscle group should remove a muscle group from database
Seeding complete
    ✓ DELETE muscle grp should not remove muscle grp w/ missing data
Seeding complete
    ✓ DELETE muscle grp should error w/ del muscle grp w/ exercises
  22 passing (2s)
 ```

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

```
Kailins-MacBook:byob kat$ npm run eslint

> byob@1.0.0 eslint /Users/kat/Documents/Turing/byob
> eslint --fix ./

```

#### Attach a screenshot of your TravisCI build passing

[TravisCI build](https://cl.ly/2Z0c261v1l1T)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you want to say?

This was a great project! 

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
