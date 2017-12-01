# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/Kalikoze/Tsunamis_API)

#### Link to the Deployed Application
[Heroku](https://tsunami-byob.herokuapp.com/)


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
[happy code](https://github.com/Kalikoze/Tsunamis_API/blob/c19566a57b2c2fcf8b261693c8ae0a01492a67cf/server.js#L23)

* Why were you proud of this piece of code?

We didn't have to add any checks or if statements.  It simply assigned a value to the variable however the user passed the token to the api.  It was nice to just be able to put it in one line.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/Kalikoze/Tsunamis_API/blob/c19566a57b2c2fcf8b261693c8ae0a01492a67cf/server.js#L185-L215)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
Not happy because you have to pass a value for all keys even though some keys are redundant i.e. waves have the property of location or state/province and country and we require all three.  When refactoring, we did cut it down considerably from what the objects were in the original data.  After working with the data more though, we believe we could cut it down to reduce redundancy even more if we had more time.  

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://user-images.githubusercontent.com/25714149/31556954-39ede6d6-b004-11e7-8316-4d9c2b0cb57c.png)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](https://user-images.githubusercontent.com/25714149/31557058-9be5009a-b004-11e7-82ed-e82257838289.png)

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://user-images.githubusercontent.com/25714149/31557096-bade2918-b004-11e7-9ba9-bd8c1b805472.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say

We ended up enjoying the project a lot more than expected.  We feel much more comfortable with backend than last week.

-----


# Instructor Feedback (Robbie)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**6 points**: (10 possible points)

- Some weird indentation in [this sample response](https://github.com/Kalikoze/Tsunamis_API/blob/master/documentation/source_GET.md)
- [Same here](https://github.com/Kalikoze/Tsunamis_API/blob/master/documentation/source_PATCH.md), be consistent with indentation size
- Great job showing what is required for endpoints and sample responses
- I like the links to multiple doc pages, helps to break up large APIs
- Not sure how useful the error section is for each endpoint, but it would be nice to have specific errors they might encounter if you're going to document errors
- I don't see any documentation on JWT auth or which endpoints require them

### Feature Completion

**60 points**: (60 possible points)

### Testing & Linting & Error Handling

**32 points**: (40 possible points)

- I like [this](https://github.com/Kalikoze/Tsunamis_API/blob/master/test/routes.spec.js#L50) in the before block - neat. You can also have a generated token set as an environment variable so you don't have to generate it every time you run your tests.
- These [404 tests](https://github.com/Kalikoze/Tsunamis_API/blob/master/test/routes.spec.js#L129-L135) are redundant; they're really testing the same thing, which is Express's built-in 404 handler
- Good [sad path test](https://github.com/Kalikoze/Tsunamis_API/blob/master/test/routes.spec.js#L166)
- [This set of tests](https://github.com/Kalikoze/Tsunamis_API/blob/master/test/routes.spec.js#L311-L335) is not necessary because you're testing the functionality of checkAuth, and you've already tested it with [this set of tests](https://github.com/Kalikoze/Tsunamis_API/blob/master/test/routes.spec.js#L195-L233), so you have already tested that checkAuth can handle the token in various ways. All you need to do is test that an endpoint can take a token one way and the others you know should work.
- Why write out the token [here](https://github.com/Kalikoze/Tsunamis_API/blob/master/test/routes.spec.js#L326)? Interpolate the token variable.
- [This test](https://github.com/Kalikoze/Tsunamis_API/blob/master/test/routes.spec.js#L671) is fine, but I'd rather see the test use an integer as an ID that doesn't exist, as opposed to a random string

### JavaScript Style

**30 points**: (40 possible points)

- Something is up with one (or both) of your editor because it's [inserting tabs instead of spaces](https://github.com/Kalikoze/Tsunamis_API/blob/master/server.js#L22-L36) - the might look like spaces in your editor, but you can see they are tabs once you look on GitHub
- [Multi-line ternaries](https://github.com/Kalikoze/Tsunamis_API/blob/master/server.js#L45-L47) can be fine, but they are tough to parse and read long into the future; oh my there are ternaries everywhere in the server file...If your ternary doesn't look like this: `let foo = bar ? true : false`, then it's probably too long to use a ternary.
- The convention for [this endpoint](https://github.com/Kalikoze/Tsunamis_API/blob/master/server.js#L38) is usually just `/authenticate`, not even using `/api/v1`
- Good error [here](https://github.com/Kalikoze/Tsunamis_API/blob/master/server.js#L42)
- Would use the plural "sources" throughout [here](https://github.com/Kalikoze/Tsunamis_API/blob/master/server.js#L57) because you are returning a collection of sources
- Don't use the trailing `/` in your [endpoints](https://github.com/Kalikoze/Tsunamis_API/blob/master/server.js#L74)
- This [section of code](https://github.com/Kalikoze/Tsunamis_API/blob/master/server.js#L95-L101) is basically the same in multiple routes with some variance (in what params are expected) - see if you can extract this functionality into a separate function for reuse

### Workflow

**15 points**: (20 possible points)

- Want to see some smaller, atomic commits

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: 143 / 170
