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

**x points**: (40 possible points) Lorem ipsum dolor set amet

### JavaScript Style

**x points**: (40 possible points) Lorem ipsum dolor set amet

- Something is up with one (or both) of your editor because it's [inserting tabs instead of spaces](https://github.com/Kalikoze/Tsunamis_API/blob/master/server.js#L22-L36) - the might look like spaces in your editor, but you can see they are tabs once you look on GitHub

### Workflow

**15 points**: (20 possible points) Lorem ipsum dolor set amet

- Want to see some smaller, atomic commits

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: x / 170
