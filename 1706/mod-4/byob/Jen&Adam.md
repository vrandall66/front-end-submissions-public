# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)
Jen & Adam

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/jenPlusPlus/build-your-own-backend)

#### Link to the Deployed Application
[Heroku](https://jen-adam-byob.herokuapp.com/)


## Completion

#### Were you able to complete the base functionality?

* Documented all available endpoints and their usage in the README?
Yes

* Seeded a database with at least 2 tables and 1 relationship?
Not yet in production. Yes for dev and test environments.

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
[happy code](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/server.js#L182-L195)

* Why were you proud of this piece of code?
Neither of us had written a patch before. It took some debugging, but we were excited to work it out! We really enjoyed writing all of the server.js file. We're pleased with the cleanliness of the code.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/test/routes.spec.js#L535-L550) 
(and other skipped tests)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
We struggled with inconsistent output depending on where we tested our code (either automated or manually). We got 3 different results for some tests between running the tests locally, testing in Postman, and the tests running on CircleCI. The lack of a production database may be affecting the CircleCI build.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](<img width="665" alt="screen shot 2017-12-15 at 12 53 14 pm" src="https://user-images.githubusercontent.com/6845268/34058101-0b7df34e-e197-11e7-9101-19430aa4ca7b.png">
)

#### Attach a screenshot of your CircleCI build passing

[circleCI build]()

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say
We enjoyed writing the server and API. We paired for much of the code, and are proud of what we wrote. The tests were not particularly difficult to write, but we had issues depending on the environment where they ran.

-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**9 points**: The README includes documentation for all available endpoints and how to use them. Instructor can easily follow the documentation for using the API.

* I like the waffle badge and the links to the project spec and heroku URL in the README.

* Nice organized tables with data types and required information. Very detailed. Would just like a littleeee more information on how to actually be authorized for a protected endpoint. 

### Feature Completion

**60 points**: Developer has implemented all 10 endpoints, 4 are secured via JWTs and one is a custom endpoint that filters data based on query params. The database is seeded with at least two tables and one relationship.

### Testing & Linting & Error Handling

**15 points**: Project has a running test suite that covers most happy and sad paths for each endpoint. Error handling has been implemented but does not cover all possible scenarios or is unhelpful for the end-user. Linter has some errors that need fixing.

* The assertions [here](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/test/routes.spec.js#L67-L79) don't really verify that the data has been filtered based on the query param. We should be checking that the objects contain a city property that actually equals dallas.

* Nice specific [error message here](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/test/routes.spec.js#L89)

* [Whomp whomp](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/test/routes.spec.js#L94-L96) for [these](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/test/routes.spec.js#L112-L118)

* We should also be asserting that the array length is 1 and that the id matches the id that was passed in through the endpoint [here](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/test/routes.spec.js#L103-L108)

* Lots of skipped tests that I have to assume are failing


### JavaScript Style

**25 points**: Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

* Let's move all of [this](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/server.js#L25-L116) out into some sort of utils or helper file, shall we?

* These [error](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/server.js#L106) messages should [be](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/server.js#L113) a llittle more specific, as they're slightly different scenarios. One of them means the user hasn't provided authorization as all, whereas the other one means they simply don't have the correct level of permissions.

* Curious what the thought process was [here](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/server.js#L135-L136). This looks like you're limiting yourself to allowing only a single query parameter, and you're depending on it being at position 0 of an array of keys in the query parameter? `request.query` in express gives you an entire object of all the key value pairs for any query parameters, and you could just use that entire object within a `where` condition of your database selection. That would allow you to automatically apply any query parameters a user has put on the end of their url.

* Duplicating [this](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/server.js#L169-L173) a lot again, break it out into a dynamic helper along with all those other functions you have at the top of the file.

* 202 is a little [weird here](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/server.js#L192), it's more common to just see a 204 returned with no json data.

* [This](https://github.com/jenPlusPlus/build-your-own-backend/blob/master/server.js#L202) isn't all that could go wrong here. There might be a generic 500 internal server error that would now be swallowed up by this 404, which might not be an accurate reflection of what went wrong.

### Workflow

**17 points**: Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of “dead” or commented-out code and debugger statements like console.log that need to be cleaned up.

* Nice use of waffle for issue tracking

* It'd be nice to squash the 23 most recent commits that all say 'Update README'...and all the other ones that are littering your history

* Nice consistent formatting of commit messages

* Initially I thought you had enough commits to be making small, atomic changesets, but given how most of your commits are Update READMEs, I have a strong feeling there are some commits in your history that include way too many changes all at once. Like [this one](https://github.com/jenPlusPlus/build-your-own-backend/commit/44dfb88fd0aa3b29f4f280722e9b4b2e1b3f85b2) that also seems to add a GET request, and fixes a commit that accidentally added merge conflict syntax...

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: 126 / 170
