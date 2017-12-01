# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB - Christie Lynam & Ana Jaureguui](https://github.com/christielynam/byob)

#### Link to the Deployed Application
[Heroku - Christie Lynam & Ana Jaureguui](https://byob-cl.herokuapp.com/)


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
[happy code](https://github.com/christielynam/byob/blob/master/server.js#L28-L76)

* Although this piece of code is a bit verbose, JWT's were a difficult concept and we are proud to have conquered this step and now have a better understanding of how to implement JWT's.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/christielynam/byob/blob/master/server.js#L155-L177)

* This was a piece of code we have been working on back and fourth for a bit. We would like to have the user be able to enter the full date with no spaces as a query param. As of now the only way it will work is to have a space between month and day "January 4".  

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

<img width="1391" alt="screenshot 2017-10-13 08 53 31" src="https://user-images.githubusercontent.com/20731901/31552257-2f487dc8-aff4-11e7-87bf-6549302447d7.png">
<img width="1391" alt="screenshot 2017-10-13 08 53 46" src="https://user-images.githubusercontent.com/20731901/31552258-3007e744-aff4-11e7-85c2-91fa34675c49.png">
<img width="1391" alt="screenshot 2017-10-13 08 54 00" src="https://user-images.githubusercontent.com/20731901/31552259-301f24d6-aff4-11e7-952e-b21f240e7fae.png">

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

<img width="679" alt="screen shot 2017-10-13 at 10 57 42 am" src="https://user-images.githubusercontent.com/20754511/31557320-7c985b50-b005-11e7-9d7f-723f48bb1e43.png">

#### Attach a screenshot of your CircleCI build passing

<img width="1365" alt="screen shot 2017-10-13 at 9 13 17 am" src="https://user-images.githubusercontent.com/20754511/31553195-dd31dbd0-aff6-11e7-95fb-57191aa6333b.png">
<img width="1362" alt="screen shot 2017-10-13 at 9 09 50 am" src="https://user-images.githubusercontent.com/20754511/31553076-839c25c6-aff6-11e7-982e-8d7c3fe86872.png">
<img width="1353" alt="screen shot 2017-10-13 at 9 10 15 am" src="https://user-images.githubusercontent.com/20754511/31553089-8ba66812-aff6-11e7-9066-bd9b18b83ff9.png">
<img width="1358" alt="screen shot 2017-10-13 at 9 10 31 am" src="https://user-images.githubusercontent.com/20754511/31553097-8feb217e-aff6-11e7-8337-2c5af7de6519.png">
<img width="1370" alt="screen shot 2017-10-13 at 9 10 42 am" src="https://user-images.githubusercontent.com/20754511/31553106-93e44ab2-aff6-11e7-908d-d1b44f62d033.png">

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say

-----


# Instructor Feedback (Robbie)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**8 points**: (10 possible points)

- Should group similar endpoints together (types: GET, DELETE, etc. and then list holidays: GET, POST, DELETE, etc.)
- Great job with example output and sample requests
- Careful with bulleted lists that only contain one bullet - defeats the purpose of a list
- For POST requests or anything else that needs information passed in the body of the request, it is good to let them know what needs to be in the body (or at least show a sample)

### Feature Completion

**60 points**: (60 possible points)

### Testing & Linting & Error Handling

**32 points**: (40 possible points)

- When going through a [number of items in an array](https://github.com/christielynam/byob/blob/master/test/routes.spec.js#L71-L82), you can use an iterator/array prototype to simplify this code and possibly extract the functionality for other tests
- [This 404 test](https://github.com/christielynam/byob/blob/master/test/routes.spec.js#L87-L94) and [this test](https://github.com/christielynam/byob/blob/master/test/routes.spec.js#L27-L34) are the same test - they're testing Express's built-in middleware to find defined endpoints, so you only need this test once, otherwise it's redundant
- For [these tests](https://github.com/christielynam/byob/blob/master/test/routes.spec.js#L277-L308), you have already tested this functionality of passing the token in various ways above, so you've tested that the checkAuth middleware is working as it should - testing all of the ways to pass in the token once is good enough, after that it is redundant and you can test the route passing the token in one way
- Do you want to be testing for any type of [error message here](https://github.com/christielynam/byob/blob/master/test/routes.spec.js#L249)?
- For [this test](https://github.com/christielynam/byob/blob/master/test/routes.spec.js#L271) and the two following this test, you should be testing the content of the object, not just that the response body is an object
- You have an [error message](https://github.com/christielynam/byob/blob/master/server.js#L64) for the test like the one above, just need to test for the message (for multiple tests)

### JavaScript Style

**32 points**: (40 possible points)

- [This](https://github.com/christielynam/byob/blob/master/server.js#L31-L41) can be a little more succinct and easier to parse through using the OR operator
- [This section](https://github.com/christielynam/byob/blob/master/server.js#L103-L109) of code is repeated throughout the server file with some variation - see if you can extract the functionality into its own function so it can be reused and DRY up the route handlers
- Be a little more specific with [this error message](https://github.com/christielynam/byob/blob/master/server.js#L147)
- Why are [these](https://github.com/christielynam/byob/blob/master/server.js#L159-L166) two separate if statements? Supplying both `fullDate` and `month` in a request will still send only one response
- Careful with throwing the [whole request body](https://github.com/christielynam/byob/blob/master/server.js#L191) (minus the token) into the database methods because you don't really know why is in the body - could be more information than you want supplied in the body and the DB might error out

### Workflow

**17 points**: (20 possible points)

- Good job with smaller commits
- The commit count looks a little lopsided in terms of equal contributes; make sure both team members are driving equally

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: 149 / 170
