# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/nogully/denver-history)

#### Link to the Deployed Application
[Heroku](http://denver-history.herokuapp.com/)


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
[happy code](https://github.com/nogully/denver-history/blob/44920fbf48bee77d31f31ad688a6895ddf813f89/test/routes.spec.js#L708-L723)

* Why were you proud of this piece of code?
We were excited to learn about JSON Web tokens and implement them. Also we had some nice 'sad path' handling on this middleware function.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/nogully/denver-history/blob/44920fbf48bee77d31f31ad688a6895ddf813f89/test/routes.spec.js#L708-L723)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
We couldn't figure out how to pass this one error handling test.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()
```
API Routes
    POST /authenticate
      ✓ should return a status of 201 and a JWT (58ms)
      ✓ should return a 422 error if a parameter is not provided
    Districts
      GET /api/v1/districts
        ✓ should return all districts
      GET /api/v1/districts/:id
        ✓ should return a specific district
        ✓ should return a 404 error if the district is not found
      GET /api/v1/districts/:id/buildings
        ✓ should return all buildings from a specific district
        ✓ should return a 404 error if there are no buildings in a district
      POST /api/v1/districts
        ✓ should create a district if the token is authorized
        ✓ should return a 422 error if the name is missing
        checkAuth
          ✓ should return a 403 error if there is no auth token
          ✓ should return a 403 error if the token is not authorized
          ✓ should return a 403 error if the user is not using an authorized email
      DELETE /api/v1/districts
        ✓ should delete a district with no buildings related to it
        ✓ should return a 404 error if the district does not exist
        ✓ should return a 422 error if there is no id provided
        ✓ should return a 500 error if it has buildings related to it
    Search
      GET /api/v1/search
        ✓ should accept search queries from the user
        ✓ should return a nice error if the query is missing parameters
        ✓ should return a nice error if that database column exists but nothing matches the search
    Buildings
      GET /api/v1/buildings
        ✓ should return all buildings
      GET /api/v1/buildings/:id
        ✓ should return a specific building
        ✓ should return a 404 error if the building does not exist
      PATCH /api/v1/buildings/:id/description
        ✓ should return a success message when the description is changed
        ✓ should return a 422 error if there is no description in the body
        ✓ should return a 422 error if the description is empty
        ✓ should return a 404 error if the target building doesnt exist
      PATCH /api/v1/buildings/:id/aka_name
        ✓ should change the aka_name of a building
        ✓ should return a 404 if the target building does not exist
        ✓ should return a 422 if there is no aka_name provided
        ✓ should return a 422 if the aka_name provided is empty
      POST /api/v1/buildings
        ✓ should create a new building
        - should return a 422 error if the user tries to add a key that is not approved
      DELETE /api/v1/buildings/
        ✓ should delete a building
        ✓ should return a 404 if the building doesnt exist
        ✓ should return a 422 if there is no id included
 ```

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.
[linter output]()
```
$ npm run eslint
> denver-history@1.0.0 eslint /home/travis/build/nogully/denver-history
> eslint *.js
The command "npm run eslint" exited with 0.
```

#### Attach a screenshot of your TravisCI build passing

[TravisCI build](https://travis-ci.org/nogully/denver-history)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you want to say?
Nora might use this API for her final project

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
