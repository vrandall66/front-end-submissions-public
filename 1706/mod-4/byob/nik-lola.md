# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/NikBorn/byob)

#### Link to the Deployed Application
[Heroku](https://boyb-byob.herokuapp.com/)


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
[happy code](https://github.com/NikBorn/byob/blob/master/server.js#L29-L56)

* Why were you proud of this piece of code?

It handles the testing env as well as authentication and authorization in one function.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/NikBorn/byob/blob/master/test/routes.spec.js#L144-L151)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
We were not getting an error message back when testing this sad path, so we took out the validation for it so the test would pass.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()
Test Seeding Complete!
      ✓ should not be able to update a bill record if the user is trying to change the id
    PATCH /api/v1/houses/:houseId/chores/:id
Test Seeding Complete!
      ✓ should be able to update a chore record
Test Seeding Complete!
      ✓ should not be able to update a bill record if the record does not exist
Test Seeding Complete!
      ✓ should not be able to update a chore record if the user is trying to change the id
    PATCH /api/v1/houses/:houseId/bulletins/:id
Test Seeding Complete!
      ✓ should be able to update a bulletin record
Test Seeding Complete!
      ✓ should not be able to update a bulletin record if the record does not exist
Test Seeding Complete!
      ✓ should not be able to update a bulletin record if the user is trying to change the id
    DELETE /api/v1/houses/:houseId/bills/:id
Test Seeding Complete!
      ✓ should delete bill with id specified
Test Seeding Complete!
      ✓ should return 422 if no bill found
    DELETE /api/v1/houses/:houseId/chores/:id
Test Seeding Complete!
      ✓ should delete chore with id specified
Test Seeding Complete!
      ✓ should return 422 if no chore found
    DELETE /api/v1/houses/:houseId/bulletins/:id
Test Seeding Complete!
      ✓ should delete bulletin with id specified
Test Seeding Complete!
      ✓ should return 422 if no bulletin found


  52 passing (4s)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output]()

Lolas-Koala-Sparkle-Machine:byob lolakoala$ npm run lint

> byob@1.0.0 lint /Users/amandabrenner/turing/mod4/byob
> eslint ./

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://github.com/NikBorn/byob/blob/master/assests/Screen%20Shot%202017-12-15%20at%2012.44.35%20PM.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say


-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**7 points**: The README includes documentation for all available endpoints and how to use them. Instructor can mostly follow the documentation for using the API.

//INTRO THE PROJECT!//

//INTRO THE PROJECT!//

//INTRO THE PROJECT!//

* ^ That could be a little more informative than it is...

* For your [post and patch requests](https://github.com/NikBorn/byob/blob/master/README.md#post-houses), I need to see an example of what kind of data I need to pass in with the request, not just the endpoint to be hit.

* Couple of typos here and there, but none that actually distract from the usage of the API


### Feature Completion

**60 points**: Developer has implemented all 10 endpoints, 4 are secured via JWTs but is missing a custom endpoint that filters data based on query params. The database is seeded with at least two tables and one relationship.

* One little feature I'm not noticing right away is the custom URL endpoints/filtering by query params. e.g. grabbing houses with an endpoint that has a query param like houses?zipCode=80205.

* ...Just kidding. I think that's what you're trying to do [here](https://github.com/NikBorn/byob/blob/master/server.js#L107-L118), but this is a bit off. You shouldn't be getting ALL bills from the database, and THEN filtering the result by a request param, you should be using a `where` condition in your database selection to only get back what already matches.

### Testing & Linting & Error Handling

**35 points**: (40 possible points) Project has a running test suite that covers all happy and sad paths for the appropriate endpoints. Error handling is informative and helpful for the end-user. The project has a linting configuration that passes with no errors.

* Looks like we're missing those 2 client-side route tests

* Remember that there's no guarantee your data will come back in a particular order unless you're specifically calling `.orderBy()` on the data that's returned. That makes assertions like [this](https://github.com/NikBorn/byob/blob/master/test/routes.spec.js#L52-L55) a little fragile. I'd rather you check the array with `.includes()` for a single object that looks like one of the values you're expecting.

* I'd also write an assertion [here](https://github.com/NikBorn/byob/blob/master/test/routes.spec.js#L62) that verifies that the ID of the object returned matches the one passed into the endpoint

* Nice specific error message [here](https://github.com/NikBorn/byob/blob/master/test/routes.spec.js#L86)

* Little confused by this [it block](https://github.com/NikBorn/byob/blob/master/test/routes.spec.js#L144-L151). It looks like it's checking for bills, but based on the structure of that endpoint, I would expect it to return a single house object rather than the bills associated with it.

* Can we assert against a specific error message [here](https://github.com/NikBorn/byob/blob/master/test/routes.spec.js#L276-L277) and [here](https://github.com/NikBorn/byob/blob/master/test/routes.spec.js#L287-L288)?

### JavaScript Style

**x points**: (40 possible points) Lorem ipsum dolor set amet

* Nice to see you [implementing other things we've gone over in class previously](https://github.com/NikBorn/byob/blob/master/server.js#L11-L16)


### Workflow

**15 points**: Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of “dead” or commented-out code and debugger statements like console.log that need to be cleaned up.

* Would like to see some use of github issues, and some conversations in the pull requests.

* [This](https://github.com/lolakoala/byob/blob/master/.DS_Store) should be in your .gitignore file

* Some commits with uninformative messages like [test](https://github.com/lolakoala/byob/commit/27a985dc023245d60ab34a5af6e76815cfaa658b) and [not sure](https://github.com/lolakoala/byob/commit/7c96655ba2a66e7989563558ea5f8154b62a0442)


## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: x / 170
