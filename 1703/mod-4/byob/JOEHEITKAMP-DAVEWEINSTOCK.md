# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the Github Repository for the Project
[BYOB](https://github.com/dstock48/byo-backend)

#### Link to the Deployed Application
[Heroku](https://winter-resort-api.herokuapp.com/)


## Completion

#### Were you able to complete the base functionality?

* Documented all available endpoints and their usage in the README?
YES

* Seeded a database with at least 2 tables and 1 relationship?
YES

* Had at least 10 endpoints that returned responses with appropriate status codes?
YES

* Secured at least 4 endpoints with JWTs?
YES

* Enforced a linter and wrote code that conformed to it?
YES

* Wrote tests for both happy and sad paths for each endpoint?
YES

* Setup automatic deployments with CircleCI to a production app on Heroku?
YES

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/dstock48/byo-backend/blob/9479202b684225496c2f71458d1b07410ca725c9/db/test/seeds/byob_test_seeds.js#L5-L30)

* Why were you proud of this piece of code?

We spent a fair amount of time working through the nested Promise.all setup to seed three databases and made consistent progress the whole time.  It was a fun puzzle that challenged us without making us want to throw the towel in.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/dstock48/byo-backend/blob/47d3945d83bd8b13ca3ae8aabf8acafdd6fdacb5/web-scraping/ski-resort-scraper.js#L31-L268)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

The website that we scraped to acquire our data had _very_ poor HTML and did not make proper use of classes. In order to select specific elements on the page that we wanted, we had to write some not-so-great feeling JS to do so. I don't necessarily know that there was a better way to do this, I just wish the website would have used more classes on their page elements.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
  JWT implemetation on API Routes
    JWT send methods
      ✓ Should return an array of states when the JWT is passed in the request header
      ✓ Should return an array of states when the JWT is passed in as a URL query param
      ✓ Should return an array of states when the JWT is passed in the request body
    SAD PATH - GET requests with no JWT
      ✓ /api/v1/states -  Should return a 403 error if the user does not pass in a JWT
      ✓ /api/v1/resorts - Should return a 403 error if the user does not pass in a JWT
      ✓ /api/v1/trails - Should return a 403 error if the user does not pass in a JWT
    SAD PATH - POST, PATCH, DELETE requests without admin access
      ✓ POST /api/v1/states - Should not allow a user without admin privileges to post a new state
      ✓ PATCH /api/v1/states/:id - Should not allow a user without admin privileges to patch a state
      ✓ DELETE /api/v1/states/:id - Should not allow a user without admin priveleges to delete a state
      ✓ POST /api/v1/resorts - Should not allow a user without admin priveleges to post a new resort
      ✓ PATCH /api/v1/resorts/:id - Should not allow a user without admin privileges to patch a resort
      ✓ DELETE /api/v1/resorts/:id - Should not allow a user without admin privileges to delete a resort
      ✓ POST /api/v1/trails - Should not allow a user without admin privileges to post a new trail
      ✓ PATCH /api/v1/trails/:id - Should not allow a user without admin privileges to patch a trail
      ✓ DELETE /api/v1/trails/:id - Should not allow a user without admin privileges to delete a trail

  API routes
    GET api/v1/resorts
      ✓ Should return an array of all resorts (98ms)
      ✓ Should return only the resorts from a specific state
      ✓ SAD PATH - Should return an error status if you do not hit the endpoint correctly
      ✓ Should return a specific resort
      ✓ SAD PATH - Should return an error message and status if no resort is found
      ✓ Should return all trails for a specific resort
      ✓ SAD PATH - Should return an error message and status if the resort is not found
    POST /api/v1/resorts
      ✓ should add a new resort to the resorts table in the database
      ✓ SAD PATH - Should return an error when not provide all required parameters
    DELETE /api/v1/resorts/:id
      ✓ should delete a specific record from the resorts table of the database (38ms)
      ✓ SAD PATH - Should return an error when trying to delete a record that does not exist
    PATCH /api/v1/resorts/:id
      ✓ should update a resort record with the supplied information
      ✓ SAD PATH - Should return an error message if you try to update the ID property of a record
      ✓ SAD PATH - Should return an error message if you try to update a resort that cannot be found

  Client Routes
    GET /
      ✓ Should return the home page with text

  API routes
    GET /api/v1/states
      ✓ Should return an array of states
      ✓ SAD PATH - Should return a 404 if the get is improperly called
    GET /api/v1/states/:stateAbbreviation
      ✓ Should return a single state based on the state abbreviation passed as a param
      ✓ Should allow a param that is case insensitive
      ✓ SAD PATH - Should return a 404 with an error message if the param doesn't exist
    GET /api/v1/states/:id/resorts
      ✓ Should return all resorts that are in a given state
      ✓ SAD PATH - Should return a 404 status with an error message if a state does not have any resorts
    POST /api/v1/states
      ✓ Should allow the addition of a new state
      ✓ Should format the state name and abbreviation properly
      ✓ SAD PATH - Should return a 500 status with an error message if a state name  already exists
      ✓ SAD PATH - Should return a 500 status with an error message if a state abbreviation already exists
      ✓ SAD PATH - Should return a 422 status with an error message if a required parameter is missing
      ✓ SAD PATH - Should return a 422 status with an error message if the state abreviation is not exactly 2 characters
      ✓ SAD PATH - Should return a 500 status with an error message if a property is posted that doesn't exist in the database
    PATCH /api/v1/states/:id
      ✓ Should update one record
      ✓ Should update multiple records
      ✓ SAD PATH - Should not allow you to update an ID
      ✓ SAD PATH - Should return an error if the state does not exist
    DELETE /api/v1/states/:id
      ✓ should delete a specific record from the states table of the database
      ✓ SAD PATH - should return an error when trying to delete a record that does not exist
      ✓ SAD PATH - should return an error if the state has a resort linked to it

  API trails routes - /api/v1/trails
    GET /api/v1/trails
      ✓ Should return an array of trails
      ✓ SAD PATH - Should return a 404 if the get is improperly called
    GET /api/v1/trails/:id
      ✓ Should return a single trail based on ID passed as a param
      ✓ SAD PATH - Should return a 404 with an error message if the ID doesn't exist
    POST /api/v1/trails
      ✓ Should allow the addition of a new trail
      ✓ SAD PATH - Should return a 422 status with an error message if a required parameter is missing
      ✓ SAD PATH - Should return a 500 status with an error message if a property is posted that doesn't exist in the database
      PATCH /api/v1/trails/:id
        ✓ Should update one record
        ✓ Should update multiple records
        ✓ SAD PATH - Should not allow you to update an ID
        ✓ SAD PATH - Should return an error if the trail does not exist
      DELETE /api/v1/trails/:id
        ✓ should delete a specific record from the trails table of the database
        ✓ SAD PATH - should return an error when trying to delete a record that does not exist


  64 passing (6s)
```

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

```
npm run lint

> web-scraping@1.0.0 lint /home/ubuntu/byo-backend
> eslint ./
```

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://github.com/dstock48/byo-backend/blob/master/public/CircleCI%20Screen%20Shot%202017-08-27%20at%2011.08.14%20PM.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say

-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**10 points**: The README includes documentation for all available endpoints and how to use them. Instructor can easily follow the documentation for using the API.

### Feature Completion

**x points**: Lorem ipsum dolor set amet

### Testing & Linting & Error Handling

**x points**: Lorem ipsum dolor set amet

### JavaScript Style

**x points**: Lorem ipsum dolor set amet


## Project is worth 150 points

## To get a 3 on this project, you need to score 110 points or higher
## To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
