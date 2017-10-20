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

**x points**: (40 possible points) Lorem ipsum dolor set amet

### JavaScript Style

**x points**: (40 possible points) Lorem ipsum dolor set amet

### Workflow

**20 points**: (20 possible points)

- Good job with small commits, looks like fairly equal contributions from both team members

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: x / 170
