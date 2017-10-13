# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the Github Repository for the Project
[BYOB](https://github.com/tylerjhevia/BYOB)

#### Link to the Deployed Application
[Heroku](https://byob-db-th.herokuapp.com/)


## Completion

#### Were you able to complete the base functionality?

* Documented all available endpoints and their usage in the README?
**Yes**

* Seeded a database with at least 2 tables and 1 relationship?
**Yes**

* Had at least 10 endpoints that returned responses with appropriate status codes?
**Yes**

* Secured at least 4 endpoints with JWTs?
**Yes**

* Enforced a linter and wrote code that conformed to it?
**Yes**

* Wrote tests for both happy and sad paths for each endpoint?
**Yes**

* Setup automatic deployments with CircleCI to a production app on Heroku?
**Yes**

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/tylerjhevia/BYOB/blob/master/beerScraper.js#L356-L398)

* We wanted to scrape beer and brewery data from ratebeer.com, so we had to find a way to loop through each individual brewery page to get the info we needed. We collected the urls that we wanted to loop through by selecting the `<a></a>` tags on the brewery index page and pushing their href values into a new array. Then we reduced the array of urls and returned an instance of nightmare for each one, where we scraped the data that we needed from the brewery page. We pushed the nightmare promises into a Promise.resolve(), and then created a new file with an array of the resolved data.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/tylerjhevia/BYOB/blob/master/server.js#L25-L56)

* Our checkAuth middleware function could definitely use some refactoring. We could find a cleaner way to check whether the token is in the body, query params, or headers.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://imgur.com/a/l8Lm8)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](https://imgur.com/a/FolLq)

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://imgur.com/a/qVQnI)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say

-----


# Instructor Feedback (Instructor Name)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**x points**: Lorem ipsum dolor set amet

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
