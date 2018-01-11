# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/hsanchez7934/hs-build-your-own-backend)

#### Link to the Deployed Application
[Heroku](https://hs-byob-12-17-2017.herokuapp.com/)


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

[happy code](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/db/seeds/dev/watches.js)
Lines 4 through 25; functions createBrands and createWatch.

* Why were you proud of this piece of code?
Took me a while to figure out how to seed the large data set that I'm using.
The first few functions that I wrote were long and sloppy but in the end I was able to end up with a few lines
of code and the functions work the way I want them to.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/test/routes.spec.js)
Lines 220 through 251

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
  These test have been problematic. I've had issues trying to debug them.  The test that begins on 220 passes when I run npm 
  test, but when circle ci starts the build process, it fails.  The second test will not pass, the only error I get
  is that I need to ensure that I call done.  I need to refactor and debug so I can fix these issues.
  
  
#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

BYOB is running on 3002.
  Client Routes
    ✓ should return the homepage with text (70ms)
    ✓ should return 404 error for nonexistent route

  API Routes
    ✓ should return a token for a user,
      if email ends in turing.io user.admin
      property should be set to true
    ✓ should return a token for a user,
      if email does not end in turing.io user.admin
      property should be set to false
    ✓ should retrieve all brands

express deprecated req.param(name): Use req.params, req.body, or req.query instead server.js:83:23
express deprecated req.param(name): Use req.params, req.body, or req.query instead server.js:84:23
    ✓ should retrieve all watch models
    ✓ should retrieve all watch models that
           match min and max parameter requirements,
           this test has a min of 0 and max of 3000
           for price range
    ✓ should return status 404 if no watches match
      the min and max parameter requirements,
      for this test the min is 0 and max is 10
    ✓ should retrieve specific brand by id number
    ✓ should retrieve specific watch by id number
    ✓ should retrieve all watch models by brand, using brand id
    ✓ should be able to post a new brand
      to watch_brands database
    - should not be able to post a new
      brand when user is not authorized
    ✓ should be able to post a new watch
      to watch_brands database
    ✓ should be able to update an existing brand
    ✓ should be able to delete brand by id
    (node:85877) UnhandledPromiseRejectionWarning: Unhandled promise rejection (rejection id: 1): Error: Internal Server Error
    ✓ should be able to delete watch by id

  17 passing (778ms)
  1 pending

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

Hector:byob hector$ npm run lint

> byob@1.0.0 lint /Users/hector/byob
> eslint ./

Hector:byob hector$

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/assets/circleci.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say

-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**7 points**: The README includes documentation for all available endpoints and how to use them. Instructor can mostly follow the documentation for using the API.

* There is very little formatting in the README which makes it a bit difficult to read, in some areas the heading formats aren't being parsed correctly. (The BYOB title for example)

* Generally you don't want to include images as part of your documentation for code...it's nice for people to be able to do a cmd+F to search for some text they're looking for. When you use images, it's impossible to do that.

* Glad you put in request body examples for your POST and PATCH requests, but I'd like you to be a little more explicit about what data type each property must be. I can infer based on the strings in the example, but it'd be nice to explicitly tell the user that.

### Feature Completion

**60 points**: Developer has implemented all 10 endpoints, 4 are secured via JWTs and one is a custom endpoint that filters data based on query params. The database is seeded with at least two tables and one relationship.

### Testing & Linting & Error Handling

**25 points**: Project has a running test suite that covers most happy and sad paths for each endpoint. Error handling has been implemented but does not cover all possible scenarios or is unhelpful for the end-user.

* Unless you're specifically calling `.order()` on your data when it's returned from the database, there's no guarantee that your data will come back in a particular order. That makes [these](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/test/routes.spec.js#L93-L97) assertions a little fragile, because it's relying on that data existing at a particular index in the array.

* Instead of doing [these loops](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/test/routes.spec.js#L120-L126) you could just check that a particular object exists in the array. Looping through is a little redundant, if you can verify that one of these objects exists in this format, it's a safe bet the rest of them exist as well.

* A 404 [here](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/test/routes.spec.js#L157-L166) is a little inaccurate. It's not that the endpoint doesn't exist, it's just that there happens to be nothing that matches the filter criteria. You could still return a 200 here but just return an empty array rather than an error.

* Assuming [these](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/test/routes.spec.js#L220-L251) are skipped because they're failing. Can't tell off the bat what the issue would be here.

* Missing lots of [catches](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/test/routes.spec.js#L280-L322) here.


### JavaScript Style

**x points**: (40 possible points) Lorem ipsum dolor set amet

* What if there was a [min but not a max?](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/server.js#L86-L91) or a max but not a min? This conditional isn't handling all possible scenarios.

* I wouldn't use ternaries in places like [this](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/server.js#L117-L121). They are harder to read. You should only use ternaries in the simplest of use cases. e.g. nothing more complex than `let foo = bar ? true : false`

### Workflow

**15 points**: Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of “dead” or commented-out code and debugger statements like console.log that need to be cleaned up.

* [This](https://github.com/hsanchez7934/hs-build-your-own-backend/blob/master/.DS_Store) should be in your .gitignore file

* 23 commits is definitely not enough for a project of this scope and size. You should have at least over 100. You should be committing smaller changesets more frequently.

* Would be good to see some use of github issues for tracking what needs to be done

* You should squash any repetitive commits like 'Update README'

* [This](https://github.com/hsanchez7934/hs-build-your-own-backend/commit/0bdd22440852de809b7465b1ad087119cf4c4e71) isn't a very helpful commit message. Line 66 means nothing to me, and it won't be line 66 forever as you start editing your application.


## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: x / 170
