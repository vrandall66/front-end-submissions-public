# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/sljohnson32/byob)

#### Link to the Deployed Application
[Heroku](https://sj-da-byob.herokuapp.com/)


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
Amazing!

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/sljohnson32/byob/blob/master/ProudCode.js)

* Why were you proud of this piece of code?
I think it awesome the user can search for schools by student teacher ratio.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/sljohnson32/byob/blob/master/SadCode.js)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
We were unsure if there was more we could do to authenticate the user and or check for authorizations.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

test suite

![image](https://user-images.githubusercontent.com/26985984/31564015-9a823fbe-b01e-11e7-8c96-2c9a1f6d92da.png)


#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

linter output

![screen shot 2017-10-13 at 12 42 20 pm](https://user-images.githubusercontent.com/26985984/31561090-01291540-b014-11e7-9d4e-58d2e253edc4.png)

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://circleci.com/gh/sljohnson32/byob)


![screen shot 2017-10-13 at 12 44 22 pm](https://user-images.githubusercontent.com/26985984/31561174-48352dde-b014-11e7-88fc-88bc25e7f909.png)


-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say
Our user side site is responsive!

-----


# Instructor Feedback (Robbie)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**7 points**: (10 possible points)

- Should make the documentation that says how to send the token in a request clearer as an Authorization header
- Leave off the trailing `/` for endpoint names, for instance `'/api/v1/districts/'` should just be listed as `'/api/v1/districts'`
- While not typical in API docs to show screenshots of tables, I like it here when there are only a few tables
- Should group similar endpoints together (districts: GET, DELETE, etc. and then list counties: GET, POST, DELETE, etc.)
- Good job noting what requests need in the body
- The placement of some images is a little off - I know this is tough with markdown, but it is looking a little messy toward the to bottom of the docs

### Feature Completion

**60 points**: (60 possible points)

### Testing & Linting & Error Handling

**32 points**: (40 possible points)

- Wouldn't leave [this comment](https://github.com/sljohnson32/byob/blob/master/test/routes.spec.js#L17) in your repo
- You can generate [these tokens](https://github.com/sljohnson32/byob/blob/master/test/routes.spec.js#L18-L28) one time somewhere, save them as environment variables, and then just bring them in to the test file as environment variables - then you don't have to generate them each time the tests are run
- Should be testing the [content of the response bodies](https://github.com/sljohnson32/byob/blob/master/test/routes.spec.js#L80), not just the length of the array but also at least looking at the properties of individual objects int he array - this goes for other tests in this file as well
- This [404 test](https://github.com/sljohnson32/byob/blob/master/test/routes.spec.js#L199) is redundant; it's really testing the same thing that you've testes [here](https://github.com/sljohnson32/byob/blob/master/test/routes.spec.js#L42), which is Express's built-in 404 handler
- [This](https://github.com/sljohnson32/byob/blob/master/test/routes.spec.js#L208) 404 test is a good test
- Not sure exactly what [this](https://github.com/sljohnson32/byob/blob/master/test/routes.spec.js#L236-L248) is really testing...The fact that you get a string back doesn't really tell you if that endpoint is doing what it should

### JavaScript Style

**30 points**: (40 possible points)

- You should not have any secret key in a [regular file](https://github.com/sljohnson32/byob/blob/master/server.js#L8) - only through an environment variable
- In this case, [this code](https://github.com/sljohnson32/byob/blob/master/server.js#L17-L20) is short enough to put all on one line
- Careful with using [all of the contents of the request body](https://github.com/sljohnson32/byob/blob/master/server.js#L45) by default because the body could contain some information that you do not want, especially if you are trying to put this data into your DB
- This [section of code](https://github.com/sljohnson32/byob/blob/master/server.js#L48-L54) is used in other routes, with slight variance - in the future, try to extract this out to a separate function that can be reused in route handlers
- Why are these separate [if statements](https://github.com/sljohnson32/byob/blob/master/server.js#L67-L78) - are there cases where you would want to run more than one condition?
- I don't think a [202 status code](https://github.com/sljohnson32/byob/blob/master/server.js#L249) is really appropriate here because the deletion has taken place. 202 codes are "The request has been accepted for processing, but the processing has not been completed.", but the deletion has taken place in the DB - it's not like you are using a cron job to schedule deletions at another time.

### Workflow

**20 points**: (20 possible points)

- Good job with small commits, looks like fairly equal contributions from both team members

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: 149 / 170
