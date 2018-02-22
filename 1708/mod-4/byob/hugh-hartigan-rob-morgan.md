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


# Instructor Feedback (Robbie)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**10 points**: (10 possible points)

### Feature Completion

**60 points**: (60 possible points)

### Testing & Linting & Error Handling

**40 points**: (40 possible points)

* Good job testing for all of the properties in the responses (along with the status codes and data structures)
* Good sad path test [here](https://github.com/HartiganHM/spirit-backend/blob/master/test/routes.spec.js#L134) with correct response
* Overall, great testing suite - very thorough

### JavaScript Style

**25 points**: (40 possible points)

* Unless there is something unique about [this endpoint](https://github.com/HartiganHM/spirit-backend/blob/master/test/routes.spec.js#L48), to get all of the terms, the route would be `/api/v1/terms` - the same thing goes for categories (this is not really a testing comment, more of a server endpoint structure comment, but I saw this in the test file first)
* [In this case](https://github.com/HartiganHM/spirit-backend/blob/master/test/routes.spec.js#L180), I think the conventional response should be a 200 with an empty array, the filter just didn't find anything matching that criteria
* [This](https://github.com/HartiganHM/spirit-backend/blob/master/test/routes.spec.js#L518) should be a 404 response since resource is not found
* [This](https://github.com/HartiganHM/spirit-backend/blob/master/test/routes.spec.js#L603) should also be a 404 because the resource is not found
* [Some good uses of middleware](https://github.com/HartiganHM/spirit-backend/blob/master/server.js#L43-L51)
* If you can, be [more specific](https://github.com/HartiganHM/spirit-backend/blob/master/server.js#L55) about what origins you are allowing to access your site than just the wildcard `*`
* Seems strange that you would have [CORS](https://github.com/HartiganHM/spirit-backend/blob/master/server.js#L73) issues in testing - would like to see more about this
* Would be great to see [this section of code](https://github.com/HartiganHM/spirit-backend/blob/master/server.js#L85-L91) pulled out into it's own function or middleware so that it can be reused (the difference being what parameters are needed for each endpoint)
* Curious why you needed to use async/await within [this request handler](https://github.com/HartiganHM/spirit-backend/blob/master/server.js#L253-L264)? And others.

### Workflow

**15 points**: (20 possible points)

* Looks like DS_STORE was committed to git, be sure to add a .gitignore right away when you create the project repository
* Would liked to have seen more, smaller commits - I would expect around 100 commits or more for a project like this

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: 150 / 170
