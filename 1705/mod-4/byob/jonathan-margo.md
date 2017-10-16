# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/mschae16/byob)

#### Link to the Deployed Application
[Heroku](https://byob-jargo.herokuapp.com/)


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

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/mschae16/byob/blob/1f09148eb1b81a98b3cece40d91c57e4057df98c/server.js#L172-L231)

* Why were you proud of this piece of code?

We are proud of this block of code, because we first had to add a new port to the ports table, and then nest a second insert into the port-usage table. Because of the way in which we structure our database for this project, we definitely got a lot of practice with nested promises.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/mschae16/byob/blob/master/server.js#L261-L273)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

We don't feel great about this block of code, because despite our delete method initially running successfully in Postman, our tests on deletion of a specific port continued to fail, and so after re-factoring and changing our migration file to include cascade onDelete functionality, our tests for this delete are still continuing to fail based on an internal server error (status 500).

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](<img width="1035" alt="screen shot 2017-10-13 at 12 34 37 pm" src="https://user-images.githubusercontent.com/25696270/31560801-f3510f14-b012-11e7-9839-beef7e6db4b4.png">)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](<img width="727" alt="screen shot 2017-10-13 at 12 31 17 pm" src="https://user-images.githubusercontent.com/25696270/31560724-ae7abcbe-b012-11e7-8d6d-7086da04feef.png">
)

#### Attach a screenshot of your CircleCI build passing

[circleCI build](<img width="1182" alt="screen shot 2017-10-13 at 12 49 34 pm" src="https://user-images.githubusercontent.com/25696270/31561411-0099e806-b015-11e7-8951-ee33950e4e77.png">)

-----

#### Please feel free to ask any other questions or make any other statements below!

We ran into the error "Unhandled rejection Error: Can't set headers after they are sent" continually while testing throughout this project. We added return statements in all of our code, and did not set headers in testing but passed token in via query parameters. The error still continues to persist.

-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**x points**:(10 possible points) Lorem ipsum dolor set amet

### Feature Completion

**60 points**: (60 possible points) Developer has implemented all 10 endpoints, 4 are secured via JWTs and one is a custom endpoint that filters data based on query params. The database is seeded with at least two tables and one relationship.

### Testing & Linting & Error Handling

**36 points**: (40 possible points) Project has a running test suite that covers all happy and sad paths for the appropriate endpoints. Error handling is informative and helpful for the end-user. The project has a linting configuration that passes with no errors.

* Nice that you broke out all your test files, but all of this required and repeated [configuration]() that you're doing should be broken out into a setup/helper file to be imported and used across test files.

* Great job testing all the possible ways someone could pass in a JWT

* Your error handling is nice and thorough, but it's also quite repetitive. I'd break out error handling like [this](237-254) into a helper function so it can be re-used among endpoints.

* Why not also give them back the [id](268) they passed in so they don't have to check elsewhere to find out.

* A PATCH should technically be able to accept any number of fields that may not [all be required](300-303). You shouldn't need this check here unless you were creating a PUT endpoint that required the entire resource object.

* Significant test coverage, though some are skipped (presumably erring out and failing CircleCI)

### JavaScript Style

**30 points**: (40 possible points) Application has exceptionally well-factored code with just slight duplication, and some areas where a different approach would simplify the logic.

* Nice, concise check for the JWT, but I'd clean up these [conditionals](37-40) a little bit by using an if/else (if there's no error, you can assume you will have a decoded token to work with)

* Not sure you need [this check here](62), both fields should be required when generating a token which you're checking for [here](76)

* You could probably simplify [this](120-128) by doing a "fuzzy" search in the database so that you don't have to do a hard transform on the value of the ship name. There's a "like" condition that Knex supports to get values that are similar to what's entered. This would allow you to just pass in the entire query object without having to do conditional checks about what's in it.


### Workflow

**x points**: (20 possible points) Lorem ipsum dolor set amet

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: x / 170
