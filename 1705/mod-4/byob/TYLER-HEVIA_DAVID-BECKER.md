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


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**x points**: Lorem ipsum dolor set amet

### Feature Completion

**60 points**: (60 possible points) Developer has implemented all 10 endpoints, 4 are secured via JWTs and one is a custom endpoint that filters data based on query params. The database is seeded with at least two tables and one relationship.

### Testing & Linting & Error Handling

**x points**: Lorem ipsum dolor set amet

* Nit pick, but a friendlier error message [here](52) would be 'You must have admin privileges to perform this operation'

* I'd still use a [422 here](61) rather than a 400

* Doesn't look like your CircleCI build is running your linter. 

* Error handling is  thorough, but repetitive. I'd break out error handling like [this](169-172) into a helper function so it can be re-used among endpoints.

### JavaScript Style

**20 points**: Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

* A simpler way to do this [check](26-44) is by assigning the token variable right away and falling back through each possible option. If none of the values stick, it will just be undefined. e.g.:

```js
let token = request.headers.authorization || request.body.token || request.query.token;
```

* Not sure you need [this check here](49), both fields should be required when generating a token which you're checking for [here](60)

* Little confused what [this](51) check is doing. The `admin` value you should be saved and stored in the decoded token, not passed into the request body. (A user should only have to pass in the token to perform admin operations, not an admin value). Rather than doing an object.assign [here](67-72) for the JSON object you're returning, you should add that `admin` value into the payload of the JWT before it even gets signed.

* [This](76-127) code can be cleaned up and refactored a bit by blah blah blah

* [This ternary](135-139) is really difficult to read. Best practices/only use case for using ternaries in a readable fashion: left-hand assignments that will be assigned one of two values. e.g. `let foo = bar ? true : false`.

* [This](146) endpoint structure is a little unRESTful -- if you want to return all beers that belond to a particular brewery, you would probably want to use a structure like `/api/v1/breweries/:id/beers`. Alternatively, since this is more of a many-to-many relationship, you could use the brewery ID as a query param and do a GET on all beers with that brewery id, like so: `/api/v1/beers?breweryID=125`

* [These properties](165-167) should not be passed in by the user for these requests. Only the token.


## Project is worth 150 points

## To get a 3 on this project, you need to score 110 points or higher
## To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
