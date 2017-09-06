# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the Github Repository for the Project
[BYOB](https://github.com/jdiejim/BYOB)

#### Link to the Deployed Application
[Heroku](https://jdj-byob.herokuapp.com/)


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

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/jdiejim/BYOB/blob/master/db/seeds/dev/data.js#L7-L36)

* Why were you proud of this piece of code?

I use recursion and promises to seed regions and industry in order. Before this I had problem with setting the id because the promises resolved at different times. With this code I was able to fix this bug.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/jdiejim/BYOB/blob/master/models/Betas.js#L114-L135)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I was able to make this query work, but I was not sure if this is the correct way to do it. It checks what type of params the request has and respond base on different scenarios.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
BYOB is running on 3000
  API Auth Routes
    POST api/v1/auth/request_token
      ✓ should return token with admin property as false if email does not end in byob.io (74ms)
      ✓ should return token with admin property as true if email ends in byob.io
      ✓ should return error if there are missing params

  API Beta Routes
    GET /api/v1/betas
      ✓ should return all betas
      ✓ should return sorted betas by ascending order when specified in query
      ✓ should return sorted betas by descending order when specified in query
      ✓ should return bad request if sort query is invalid
      ✓ should return all betas of specific industry when queried
      ✓ should return all betas of specific region when queried
      ✓ should return beta of specific industry and region when queried
      ✓ should return not found if query does not exist
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
    POST /api/v1/betas
      ✓ should create new beta
      ✓ should not create a new beta if missing parameters
      ✓ should not create a new beta if required parameters have wrong syntax
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
      ✓ should return error if non-admin token attached
    GET /betas/:id
      ✓ should return beta matching the id param
      ✓ should return not found if id does not match
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
    GET /betas/industry/:industry_id
      ✓ should return all betas for a specified industry
      ✓ should return not found if industry does not exist
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
    GET /betas/region/:region_id
      ✓ should return all betas for a specified region
      ✓ should return not found if region does not exist
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
    GET /betas/industry/:industry_id/region/:region_id
      ✓ should return all betas for a specified industry and region
      ✓ should return not found if industry or region does not exist
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
    Patch /betas/:id
      ✓ should update beta props
      ✓ should not update beta if id does not match
      ✓ should return bad request error if params have wrong syntax
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
      ✓ should return error if non-admin token attached
    Delete /betas/:id
      ✓ should delete beta
      ✓ should not delete beta if id does not match
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
      ✓ should return error if non-admin token attached

  API Industry Routes
    GET /api/v1/industry
      ✓ should return all industry names
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
    POST /api/v1/industry
      ✓ should create new industry
      ✓ should not create new industry if missing parameter
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
      ✓ should return error if non-admin token attached
    PUT /api/v1/industry/:id
      ✓ should update the name of an industry
      ✓ should not update the name of an industry if missing parameter
      ✓ should return not found if industry does not exists
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
      ✓ should return error if non-admin token attached
    DELETE /api/v1/industry/:id
      ✓ should delete an industry
      ✓ should return not found if industry does not exists
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
      ✓ should return error if non-admin token attached

  API Region Routes
    GET /api/v1/region
      ✓ should return all region names
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
    POST /api/v1/region
      ✓ should create new region
      ✓ should not create new region if missing parameter
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
      ✓ should return error if non-admin token attached
    PUT /api/v1/region/:id
      ✓ should update the name of a region
      ✓ should not update the name of region if missing parameter
      ✓ should return not found if region does not exists
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
      ✓ should return error if non-admin token attached
    DELETE /api/v1/region/:id
      ✓ should delete a region
      ✓ should return not found if region does not exists
      ✓ should return error if no token attached
      ✓ should return error if invalid token attached
      ✓ should return error if non-admin token attached


  84 passing (3s)
```

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

```
> byob@1.0.0 lint /Users/JDJim/Documents/Turing/projects/mod4/byob
> eslint ./

```

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://github.com/jdiejim/BYOB/blob/master/screenshots/circle.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

To get an admin token the email needs to end in @byob.io

-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**8 points**: The README includes documentation for all available endpoints and how to use them. Instructor needs some clarification when following the documentation for using the API.

* [This](https://github.com/jdiejim/BYOB/blob/master/docs/endpoints/post_region.md#requires-authentication) is a little vague. I'd like to see an example of how to do this written out in code.

* I like that you've denoted required parameters [here](https://github.com/jdiejim/BYOB/blob/master/docs/endpoints/post_betas.md#parameters) but I'd also like to know what data type each param is. e.g. should I be passing in a string or integer?

### Feature Completion

**x points**: Lorem ipsum dolor set amet

### Testing & Linting & Error Handling

**38 points**: Project has a running test suite that covers all happy and sad paths for the appropriate endpoints. Error handling is informative and helpful for the end-user. The project has a linting configuration that passes with no errors.

* [.catches!!](https://github.com/jdiejim/BYOB/blob/master/test/betas.spec.js#L16-L23)

* I'd set [these](https://github.com/jdiejim/BYOB/blob/master/test/betas.spec.js#L8-L10) as environment variables in a `.env` file or something similar. Not that they need to be super secure, but it's still nice to pull them out of the codebase and hardcode a single value rather than regenerating one every time your tests run.

### JavaScript Style

**x points**: Lorem ipsum dolor set amet


## Project is worth 150 points

## To get a 3 on this project, you need to score 110 points or higher
## To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
