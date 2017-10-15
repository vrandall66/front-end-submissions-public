# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/lcaroselli/Poke150-api)

#### Link to the Deployed Application
[Heroku](https://poke150-api.herokuapp.com/) - error on deployment


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
[happy code](https://github.com/lcaroselli/Poke150-api/blob/master/server.js#L67)

* Why were you proud of this piece of code?
It took me a little bit to understand query parameters and how to implement them, so I was proud of myself when I finally understood how to add a query parameter to an end point. 

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/lcaroselli/Poke150-api/blob/master/test/routes.spec.js#L192)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
I kept getting a 500 error whenever I tried to test the response I got back in my tests. I asked for help from several people, but we couldn't quite figure out what was going on.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[tests](https://github.com/lcaroselli/Poke150-api/blob/master/assets/test.png)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](https://github.com/lcaroselli/Poke150-api/blob/master/assets/lint.png)

#### Attach a screenshot of your CircleCI build passing

[circleCI build]() - At the moment, it is not passing. 

-----

#### Please feel free to ask any other questions or make any other statements below!

This project was a lot to do alone, but it forced me to really solidify all the concepts we learned to this point, and I appreciate that. I feel like I could have gotten more accomplished more quickly with a project partner, or if I had been able to join another group.

I notified Robbie about my circlCI build failing on deployment to Heroku, but neither of us could figure out what was going on. The build was successful to a point and keeps giving me an error about the tip of the branch not being up to date, even though it is. 

-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**x points**:(10 possible points) Lorem ipsum dolor set amet

### Feature Completion

**x points**: (60 possible points) Lorem ipsum dolor set amet

* Nice to see multiple migration files in your database directory, it proves you are doing things the right way rather than just rolling back to resolve any errors in your schema.

* Your circle.yml file is having some issues with the test section - indentation is off after the 'override' statement and might be causing failures there. You also need to be running your linter in circleCI and should add a command to do so

* Will check back in re: deployment errors and see if we can't figure anything out together

### Testing & Linting & Error Handling

**30 points**: (40 possible points)  Project has a running test suite that covers most happy and sad paths for each endpoint. Error handling has been implemented but messages are sometimes more vague than they should be. Assertions could also be a bit more robust within your test suite.

* Better, more common error message to see [here](42) would be something like 'You do not have admin privileges to perform this operation'. Users don't think in terms of 'endpoints', they think in terms of what they're trying to do.

* Your error handling is nice and thorough, but it's also quite repetitive. I'd break out error handling like [this](195-201) into a helper function so it can be re-used among endpoints.

* [This](234) is a weak error message and could be made a bit more specific.

* [This 404 test](L68-L75) is redundant. You only need to do one 404 test for an endpoint that doesn't exist, doesn't matter if it is prefixed with `api/v1` or not.

* Why not give the user back the [id](272) they passed in so they don't have to go check elsewhere to see what they requested?

* I'd also assert that the error message [here](177) comes back as something that makes sense.

* I'd make an additional assertion [here](193) for what's actually in the object. Gives other developers some insight into how the code works without having to actually look through it.


### JavaScript Style

**x points**: (40 possible points) Lorem ipsum dolor set amet

* Nice organization of all your [setup, configuration and imports](1-25)

* Would be better (and still simple) to allow users to submit their token with requests in all three places (headers, queries, bodies). You could do that check and assign the token value with a single line:

```js
let token = request.headers.authorization || request.body.token || request.query.token;
```

* I'd move this [checkQuery](70-76) function out into a helper file. It's a little weird to be defining it and then calling in right away on the next line. You're also using it in multiple places, so it would be good to cut down on that duplication.

* I don't necessarily agree with returning a 404 [here](82). A 404 means nothing exists at that particular endpoint, and usually signifies that someone entered an incorrect URL. In this case, the endpoint is correct, and a resource *does* happen to exist there, it's just an empty array.

* I wouldn't put linebreaks between your [.thens](137) and [.catches](144). It breaks up the flow of the promise and makes it more difficult to read because now they look like separate, isolated operations rather than a single promise.


### Workflow

**x points**: (20 possible points) Lorem ipsum dolor set amet

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: x / 170
