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
