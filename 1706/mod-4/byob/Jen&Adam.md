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

**x points**: (60 possible points) Lorem ipsum dolor set amet

### Testing & Linting & Error Handling

**x points**: (40 possible points) Lorem ipsum dolor set amet

### JavaScript Style

**x points**: (40 possible points) Lorem ipsum dolor set amet

### Workflow

**17 points**: Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of “dead” or commented-out code and debugger statements like console.log that need to be cleaned up.

* Nice use of waffle for issue tracking

* It'd be nice to squash the 23 most recent commits that all say 'Update README'...and all the other ones that are littering your history

* Nice consistent formatting of commit messages

* Initially I thought you had enough commits to be making small, atomic changesets, but given how most of your commits are Update READMEs, I have a strong feeling there are some commits in your history that include way too many changes all at once. Like [this one](https://github.com/jenPlusPlus/build-your-own-backend/commit/44dfb88fd0aa3b29f4f280722e9b4b2e1b3f85b2) that also seems to add a GET request, and fixes a commit that accidentally added merge conflict syntax...

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: x / 170
