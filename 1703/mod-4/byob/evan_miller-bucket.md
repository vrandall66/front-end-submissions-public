# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the Github Repository for the Project
[BYOB](https://github.com/EvanSays/byob)

#### Link to the Deployed Application
[Heroku](https://byob-crspr.herokuapp.com/)


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
[happy code](https://github.com/EvanSays/byob/blob/master/server/server.js#L60)

* Why were you proud of this piece of code?

We were happy to get the query params to work dynamically.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/EvanSays/byob/blob/master/db/seeds/dev/crisprseed.js)


* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

We've been having problems with pulling down eachothers code and changing the file name to our seed file. It could of been caused from us deleting it in the begining. Lesson learned.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.


```
> byob@1.0.0 test /Users/evanmiller/Documents/turing/assignments/4-mod/byob
> NODE_ENV=test SECRET_KEY=test ./node_modules/.bin/mocha



Server is running on 6333
  Client Routes
    ✓ 01: should return a homepage with text
    ✓ 02: should return status 404

  API Routes
    GET /genes
Re-seed complete!
      ✓ 01: should get all genes from database
    POST /genes
Re-seed complete!
      ✓ 01: should be able to post to genes (44ms)
Re-seed complete!
      ✓ should not create gene with missing data
    GET /journals/:pubmed/genes
Re-seed complete!
      ✓ 01: should get a gene response based on the pubmed id
Re-seed complete!
      ✓ should not get genes with wrong pubmed id
    DELETE /journals/:pubmed/genes
Re-seed complete!
      ✓ should delete genes
Re-seed complete!
      ✓ should not delete genes with wrong pubmed
    DELETE /genes/:id
Re-seed complete!
      ✓ should delete all data pertaining to the id entered in the params
Re-seed complete!
      ✓ should not delete if required params are incorrrect
    PATCH /genes/:id
Re-seed complete!
      ✓ should update a gene
Re-seed complete!
      ✓ should not update a gene
    GET genes/id
Re-seed complete!
      ✓ should get a gene
Re-seed complete!
      ✓ should not retrieve a gene without proper id
    QUERY genes
Re-seed complete!
      ✓ should search by query
Re-seed complete!
      ✓ should not return a wrong query

  API Routes
    POST /admin
Re-seed complete!
      ✓ 01: should return a jwt encrypted token
Re-seed complete!
      ✓ 02: should break when improper values (appName) are passed
Re-seed complete!
      ✓ 03: should break when improper values (email) are passed
Re-seed complete!
      ✓ 04: should deny patch priveledges when admin:false
    POST /journals
Re-seed complete!
      ✓ 01: should add journal
Re-seed complete!
      ✓ 02: should not add journal with missing params
Re-seed complete!
      ✓ 03: should not POST when invalid values are passes
      GET /journals
Re-seed complete!
        ✓ 01: should return all journals
    POST /journals
Re-seed complete!
      ✓ 01: should return a journal based on pubmed param
    PATCH /api/v1/journals/pubmed
Re-seed complete!
      ✓ 01: should patch journals
Re-seed complete!
      ✓ 02 should not patch journals without admin privledges
    GET /journals:id
Re-seed complete!
      ✓ should retrieve a journal
Re-seed complete!
      ✓ should not retrieve a journal without a proper id


  30 passing (1s)
```

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.


```
byob@1.0.0 lint /Users/evanmiller/Documents/turing/assignments/4-mod/byob
eslint ./

```

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://www.dropbox.com/s/c43xwofr3dor78y/Screenshot%202017-08-27%2017.16.29.png?dl=1)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say

-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**8 points**: The README includes documentation for all available endpoints and how to use them. Instructor needs some clarification when following the documentation for using the API.

* Not sure if the hyphens [here](https://github.com/EvanSays/byob/blob/master/docs/GET_genes_id.md#parameters) indicated you were planning on adding additional information or not, but that's how it appears. It would be good to add the data type of all the params so I know when to pass through an integer vs string, etc. I'd also like to know exactly which parameters are required. "One or more" isn't super helpful.

### Feature Completion

**60 points**: Developer has implemented all 10 endpoints, 4 are secured via JWTs and one is a custom endpoint that filters data based on query params. The database is seeded with at least two tables and one relationship.

### Testing & Linting & Error Handling

**35 points**: Project has a running test suite that covers all happy and sad paths for the appropriate endpoints. Error handling is informative and helpful for the end-user. The project has a linting configuration that passes with no errors.

* Whomp whomp what's this [file](https://github.com/EvanSays/byob/blob/master/test/testData.js) doing?

* Where is your [.catch](https://github.com/EvanSays/byob/blob/master/test/genesServerTest.spec.js#L38-L42)? Also, while this code works, it's probably still better to break the `migrate.latest` out into a `before` block. Even though it essentially won't do anything assuming the database is up-to-date, it's still adding uncessary time to your test runner.

* You shouldn't have to do this [double request](https://github.com/EvanSays/byob/blob/master/test/genesServerTest.spec.js#L184-L189) to test endpoints that require authentication. Simply pass in a valid JWT that has been previously generated and won't expire (you'd set this as an environment variable in a .env file or something of the sort). Doing multiple requests in a single test is error prone and muddies the cause of errors.

* If you're going to break out your tests into multiple files, I'd also move all of these [authentication tests](https://github.com/EvanSays/byob/blob/master/test/journalsServerTest.spec.js#L23-L74) into their own file as they're not directly related to journals.

### JavaScript Style

**x points**: Lorem ipsum dolor set amet


## Project is worth 150 points

## To get a 3 on this project, you need to score 110 points or higher
## To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150