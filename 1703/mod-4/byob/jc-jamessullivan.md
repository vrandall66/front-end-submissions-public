# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the Github Repository for the Project
[BYOB](https://github.com/the-oem/byob)

#### Link to the Deployed Application
[Heroku](https://fotofinder.herokuapp.com/)


## Completion

#### Were you able to complete the base functionality?

* Documented all available endpoints and their usage in the README?
(Yes)

* Seeded a database with at least 2 tables and 1 relationship?
(Yes)

* Had at least 10 endpoints that returned responses with appropriate status codes?
(Yes)

* Secured at least 4 endpoints with JWTs?
(Yes)

* Enforced a linter and wrote code that conformed to it?
(Yes)

* Wrote tests for both happy and sad paths for each endpoint?
(Yes)

* Setup automatic deployments with CircleCI to a production app on Heroku?
(Yes)

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/the-oem/byob/blob/master/utils/data/exifMiner.js)

* Why were you proud of this piece of code?
_We didn't have a ready-to-download set of data to populate out API with, so we had to go about writing code to
extract EXIF data from our own photos. In addition to that, we leveraged multiple JSON packages to turn
EXIF gps data into decimal lat/lon values to be populated in the locations data table. Fun stuff that we are proud of!_

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/the-oem/byob/blob/master/src/Client/scripts.js)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
_The challenges we faced were time, with everything else going on. We would have liked to have spent
more time on this interface and the JS for it._

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

![test suite](https://the-oem.github.io/assets/byob/tests-passing.png)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

![linter output](https://the-oem.github.io/assets/byob/linter-passing.png)

#### Attach a screenshot of your CircleCI build passing

![circleCI build](https://the-oem.github.io/assets/byob/circle-ci-passing.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

Nothing else to add :)

-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**8 points**: The README includes documentation for all available endpoints and how to use them. Instructor needs some clarification when following the documentation for using the API.

* [This](https://github.com/the-oem/byob/blob/master/docs/POST_locations.md#parameters) is pretty vague. What are the params? What are their data types? I wouldn't know how to construct this object if it was the first page of documentation I landed on.

### Feature Completion

**60 points**: Developer has implemented all 10 endpoints, 4 are secured via JWTs and one is a custom endpoint that filters data based on query params. The database is seeded with at least two tables and one relationship.

### Testing & Linting & Error Handling

**35 points**: Project has a running test suite that covers all happy and sad paths for the appropriate endpoints. Error handling is informative and helpful for the end-user. The project has a linting configuration that passes with no errors.

* [First things first](https://github.com/the-oem/byob/blob/master/test/integration/cameras.routes.spec.js#L21-L38), always always always have a `.catch()` with your `.thens()`. Second, don't do rollbacks on your schema during your tests. This puts your database in an out-of-date version and you'll be testing against the wrong things. (I know everyone grabbed this code from a blog post, that blog post assumes you only have a single migration - in most cases you'll have many and this rollback will only bring you back one stop.) You're undoing this by migrating latest immediately after the rollback any way, so it's not really giving you anything useful. Third, it's probably still better to break the `migrate.latest` out into a `before` block. Even though it essentially won't do anything assuming the database is up-to-date, it's still adding uncessary time to your test runner.

* Nitpick, but I'd suggest making these [invalid query params](https://github.com/the-oem/byob/blob/master/test/integration/locations.routes.spec.js#L76) even more obviously invalid. It would be really easy to miss the typo in here and be confused about what the test is actually supposed to be asserting. A tiny typo like this doesn't signify the intent as much as a huge one would.

* Little confused why you would [query the database here first](https://github.com/the-oem/byob/blob/master/test/integration/locations.routes.spec.js#L173-L187) instead of just making the call to update based on an ID passed in as a query param. This extra step makes your test more error prone and will make it more difficult to identify the true source of a bug if it ever fails.

* Might want to put things like [this](https://github.com/the-oem/byob/blob/master/test/integration/photos.routes.spec.js#L1-L4) in your eslint config file so you don't have to copy/update them across all your test files.


### JavaScript Style

**30 points**:  Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

* [This](https://github.com/the-oem/byob/blob/master/src/server/authController.js#L8-L15) is maybe a little overengineered. It's not the best idea to have a ternary produce values that are of different data types. I'd rather `admin` just be a Boolean value that's toggled in that ternady, then do an `Object.assign` with `{ admin }`.

* I would avoid passing the token through as [a dynamic portion of the URL](https://github.com/the-oem/byob/blob/master/src/server/router.js#L13) and would prefer to see it required in the header or as a query parameter. This setup makes your URLs a bit unRESTful, as when I think about deleting a resource, I would expect the endpoint to be `/api/v1/cameras/:id`.

* Returning your responses with a [status](https://github.com/the-oem/byob/blob/master/src/server/cameraController.js#L7-L13) property is a bit redundant. Each response from a fetch request automatically comes back with an `ok` flag that's either true or false and would essentially do the same thing.

* [Ahhhh](https://github.com/the-oem/byob/blob/master/src/server/cameraController.js#L19-L27) this ternary is really difficult to read. Best practices/only use case for using ternaries in a readable fashion: left-hand assignments that will be assigned one of two values of the same data type. e.g. `let foo = bar ? true : false`.  That's about it. (True/false could be replaced with any two values, but generally you want them to be the same data type)

* Code like [this](https://github.com/the-oem/byob/blob/master/src/server/locationController.js#L54-L63) is all over the place and could be broken out into a helper file for error handling.


## Project is worth 150 points

## To get a 3 on this project, you need to score 110 points or higher
## To get a 4 on this project, you need to score 130 points or higher

# Final Score: 133 / 150
