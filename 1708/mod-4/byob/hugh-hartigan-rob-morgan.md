# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/HartiganHM/spirit-backend)

#### Link to the Deployed Application
[Heroku](https://spirit-be.herokuapp.com/)


## Completion

#### Were you able to complete the base functionality?

* Documented all available endpoints and their usage in the README?
Yes [spirit-backedn/README.md](https://github.com/HartiganHM/spirit-backend/blob/master/README.md)

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
[Happy Code](https://github.com/HartiganHM/spirit-backend/blob/4acf508722691a5de0a5691e4ee4e686aae5927d/server.js#L84-L102)

* Why were you proud of this piece of code?

We were proud of this piece of code because, outside of authenticating a new user, we also build a conditional check for the required parameters, as well as an `environment` check to ensure that authentication wasn't required in the testing environment.


#### Link to a specific block of your code on GitHub that you feel not great about
[Sad Code](https://github.com/HartiganHM/spirit-backend/blob/4acf508722691a5de0a5691e4ee4e686aae5927d/db/data/terms.js#L4-L10)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

Overall, we are very happy with all of our code and don't have anything that we are necessarily 'sad' about. However, after having built out all of the data, we realized that the `imageURL` property for each `term` object wasn't as necessary as we had anticipated. While this isn't a huge problem, having caught this sooner would have saved us time when building out our data set.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://i.imgur.com/4McZZDs.png)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](https://i.imgur.com/HZLrTd3.png)

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://i.imgur.com/Q5RCfi0.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

We would love more guidance on how to set an environment variable in Heroku/CircleCI!

-----


# Instructor Feedback (Instructor Name)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**x points**:(10 possible points) Lorem ipsum dolor set amet

### Feature Completion

**x points**: (60 possible points) Lorem ipsum dolor set amet

### Testing & Linting & Error Handling

**x points**: (40 possible points) Lorem ipsum dolor set amet

### JavaScript Style

**x points**: (40 possible points) Lorem ipsum dolor set amet

### Workflow

**x points**: (20 possible points) Lorem ipsum dolor set amet

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: x / 170
