# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/michellehoffman/build-your-own-backend)

#### Link to the Deployed Application
[Heroku](https://byob-pichelle.herokuapp.com/)


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
[happy code](https://github.com/michellehoffman/build-your-own-backend/blob/7dfa8a552ea47c21b183832dca1fdd8f78213d7b/server.js#L57-L81)

* Why were you proud of this piece of code?
We had no idea how to implement a custom query url and are proud that we were able to get it to work without hard-coding the type of data that was coming in from the query params (i.e. county).


#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/michellehoffman/build-your-own-backend/blob/7dfa8a552ea47c21b183832dca1fdd8f78213d7b/public/scripts.js#L3-L25)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
This code could have been cleaned up a bit more and not have been an anonymous function.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
Server is running on 3000
  Client Routes
    ✓ should return the homepage with text
    ✓ should return a 404 if page does not exist

  API Routes
    GET /api/v1/locations
Seeding complete!
      ✓ should return all of the locations
Seeding complete!
      ✓ should return all of the locations at a custom city query
Seeding complete!
      ✓ should return all of the locations at a custom county query
Seeding complete!
      ✓ should return all of the locations at a custom query for both city and county
Seeding complete!
      ✓ should return a 404 error if custom city query does not exist in database
Seeding complete!
      ✓ should return a 404 error if custom county query does not exist in database
Seeding complete!
      ✓ should return a 404 error if custom city and county query does not exist in database
    GET /api/v1/locations/:id
Seeding complete!
      ✓ should return a specific location
Seeding complete!
      ✓ should return a 404 error if that id does not exist
    POST /api/v1/locations
Seeding complete!
      ✓ should create a new location
Seeding complete!
      ✓ should return a 403 error if a token is not provided
Seeding complete!
      ✓ should return a 403 error if a token is invalid
Seeding complete!
      ✓ should return a 422 error if a body property is missing
    PATCH /api/v1/locations/:id
Seeding complete!
      ✓ should update an existing location with given information
Seeding complete!
      ✓ should return a 403 error if a token is not provided
Seeding complete!
      ✓ should return a 403 error if a token is invalid
Seeding complete!
      ✓ should return a 404 if location without given id does not exist
    DELETE /api/v1/locations/:id
Seeding complete!
      ✓ should delete a location from the database
Seeding complete!
      ✓ should return a 403 error if a token is not provided
Seeding complete!
      ✓ should return a 403 error if a token is invalid
Seeding complete!
      ✓ should return a 404 error if no location with that id exists
    GET /api/v1/sites
Seeding complete!
      ✓ should return all of the sites
    GET /api/v1/sites/:id
Seeding complete!
      ✓ should return a specific site
Seeding complete!
      ✓ should return a 404 error if that id does not exist
    POST /api/v1/sites
Seeding complete!
      ✓ should create a new site
Seeding complete!
      ✓ should return a 403 error if a token is not provided
Seeding complete!
      ✓ should return a 403 error if a token is invalid
Seeding complete!
      ✓ should return a 422 error if a body property is missing
    PATCH /api/v1/sites/:id
Seeding complete!
      ✓ should update an existing site with given information
Seeding complete!
      ✓ should return a 403 error if a token is not provided
Seeding complete!
      ✓ should return a 403 error if a token is invalid
Seeding complete!
      ✓ should return a 404 if site without given id does not exist
    DELETE /api/v1/sites/:id
Seeding complete!
      ✓ should delete a site from the database
Seeding complete!
      ✓ should return a 403 error if a token is not provided
Seeding complete!
      ✓ should return a 403 error if a token is invalid
Seeding complete!
      ✓ should return a 404 error if no site with that id exists


  38 passing (2s)
```

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

```
> build-your-own-backend@1.0.0 lint /Users/michellehoffman/Desktop/Turing/Module-4/Projects/build-your-own-backend
> ./node_modules/eslint/bin/eslint.js ./public/*/*.js
```

#### Attach a screenshot of your TravisCI build passing

![TravisCI build](https://github.com/michellehoffman/build-your-own-backend/blob/master/Screen%20Shot%202018-04-01%20at%2010.08.46%20PM.png)

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
