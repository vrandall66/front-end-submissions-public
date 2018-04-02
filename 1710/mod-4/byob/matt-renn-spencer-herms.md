# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/PreciseSlice/trump-ipsum)

#### Link to the Deployed Application
[Heroku](https://trump-ipsum-backend.herokuapp.com/)


## Completion

#### Were you able to complete the base functionality?

* Documented all available endpoints and their usage in the README?

	* Yes

* Seeded a database with at least 2 tables and 1 relationship?

	* Yes

* Had at least 10 endpoints that returned responses with appropriate status codes?
	
	* Yes

* Secured at least 4 endpoints with JWTs?

	* Yes

* Enforced a linter and wrote code that conformed to it?

	* Yes

* Wrote tests for both happy and sad paths for each endpoint?
	
	* Yes

* Setup automatic deployments with CircleCI to a production app on Heroku?
	
	* Yes 

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/PreciseSlice/trump-ipsum/blob/a582abba62a8247ce7d4863fbdd5524be5cfce48/server.js#L35-L69)

* Why were you proud of this piece of code?

We enjoyed solving how to implement end endpoint with custom query parameters.

We also had fun making the documentation and furthering our markdown skills.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/PreciseSlice/trump-ipsum/blob/a582abba62a8247ce7d4863fbdd5524be5cfce48/test/routes.spec.js#L216-L225)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

This test took longer than it should have get working.  We ended up implementing cascade delete in our database.  Not sure if that is the best way to handle deleting an item which still has other items using it as a foreign reference. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://i.imgur.com/6O7QBiH.png)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](https://i.imgur.com/qneUemc.png)

#### Attach a screenshot of your Travis CI build passing

[Travis CI build](https://i.imgur.com/U6GmFLs.png)

-----


# Instructor Feedback (Instructor Name)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**x points**: (10 possible points)

### Feature Completion

**x points**: (60 possible points)

### Testing & Linting & Error Handling

**x points**: (40 possible points)

### JavaScript Style

**x points**: (40 possible points)

### Workflow

**x points**: (20 possible points)

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: x / 170
