# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/tmcjunkinmarquis/byob)

#### Link to the Deployed Application
[Heroku](https://dashboard.heroku.com/apps/byob-marika-theresa)


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
[happy code](https://github.com/tmcjunkinmarquis/byob/commit/f5f9ac8b3c6f914f0aec8d5f86d2a40699c5aad9)

* Why were you proud of this piece of code?
Theresa was really helpful in trouble shooting how we hard-coded our data in to our test database to avoid mis-seeding that occurs in our development database.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/tmcjunkinmarquis/byob/commit/26e69bff32d184ef9a4c950b1d40b0c1309071bf)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
Logically, this makes sense to me in terms of seeding our database.  We create one state, then two senators so they can have corresponding ids.  However, this function does not seed consistently each time and we foudn that senator order was changing each time we seeded/re-seeding the test database.  We still don't understand why it works the way it does. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
```console
byob is running on 3000.
  API Routes
    GET /api/v1/states
      ✓ should return all states
      ✓ should return a 404 for a route that does not exist
    GET /api/v1/senators
      ✓ should return all senators
      ✓ should return a 404 for a route that does not exist
    GET /api/v1/senators/:id
      ✓ should return a single senator
      ✓ should return a 404 for a route that does not exist
    GET /api/v1/states/:id
      ✓ should return a single state
      ✓ should return a 404 for a route that does not exist
    POST /api/v1/authorize
      ✓ should give a web token if the input is right
    POST /api/v1/states
      ✓ should add a state
    PATCH /api/v1/states/:id
      ✓ should update a state
      ✓ should not update a state if there is an id field in the request
      ✓ should return a 404 for a route that does not exist
    PATCH /api/v1/senators/:id
      ✓ should update a senator
      ✓ should not update a senator if there is an id field in the request
      ✓ should return a 404 for a route that does not exist
    DELETE /api/v1/senators/:id
      ✓ should delete a senator
      ✓ should return a 404 for a route that does not exist
    DELETE /api/v1/states/:id
      ✓ should delete a state
      ✓ should return a 404 for a route that does not exist


  20 passing (1s)
```


#### Attach a screenshot or paste the output from your terminal of the result of your linter running.
```console 
 /Users/tmarq/turing/Mod4/byob/server.js
  104:1  warning  Line 104 exceeds the maximum line length of 120  max-len
  122:1  warning  Line 122 exceeds the maximum line length of 120  max-len
  140:1  warning  Line 140 exceeds the maximum line length of 120  max-len
  210:3  error    Unexpected console statement                     no-console

/Users/tmarq/turing/Mod4/byob/public/scripts.js
  25:23  error  Unexpected console statement  no-console

✖ 5 problems (2 errors, 3 warnings)
```

#### Attach a screenshot of your TravisCI build passing

![TravisCI build]( https://github.com/tmcjunkinmarquis/byob/blob/master/Screen%20Shot%202018-09-02%20at%203.37.16%20PM.png)

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
