# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the Github Repository for the Project
[BYOB](https://github.com/lindsaywparker/byob)

#### Link to the Deployed Application
[Heroku](https://lwp-byob.herokuapp.com/)


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
[happy code](https://github.com/lindsaywparker/byob/blob/master/controller.jsL64-L82)

* Allows user to input an array of objects so long as they have name property in each index, and apply the changes to the applicable location, no need to get each id first. 

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/lindsaywparker/byob/blob/master/controller.jsL36-L48)

* Ideally it shold allow posts to the state, city, and metro tables, rather than be limited to zip and neighborhood

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://github.com/lindsaywparker/byob/blob/master/test-results.png)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](https://github.com/lindsaywparker/byob/blob/master/linter-results.png)

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://github.com/lindsaywparker/byob/blob/master/CircleCI.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

environment variables in circleCI are a thing

-----


# Instructor Feedback (Instructor Name)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**9 points**: The README includes documentation for all available endpoints and how to use them. Instructor can easily follow the documentation for using the API.

* It would be good to add the data type of all the params so I know when to pass through an integer vs string, etc. You can do this directly alongside the name of the parameter in parens.

* I'd separate out the formatting of your required params vs. optional params so that they're in unique lists.

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
