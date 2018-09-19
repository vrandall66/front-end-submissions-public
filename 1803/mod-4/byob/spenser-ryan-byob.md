# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB]()

#### Link to the Deployed Application
[Heroku](https://spenser-ryan-byob.herokuapp.com/)


## Completion

#### Were you able to complete the base functionality?

* Documented all available endpoints and their usage in the README?
Yes

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

* Setup automatic deployments with TravisCI to a production app on Heroku?
Yes

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code]()

* Why were you proud of this piece of code?

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/spenserleighton1/byob/blob/802868ddd5137365fb7b8c8542be09aa0761fe70/server.js#L235)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
needs error handling.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

B.Y.O.B. is running on 3000.
  /api/v1/state_info
    ✓ shold GET all state info
    ✓ should GET a single states info
    ✓ should throw an error when passed a wrong state id
    ✓ should GET a states info based on query params
    ✓ should throw an error when passed an incorrect query parameter
    ✓ should POST state_info
    ✓ should throw an error if a required POST param is missing
    ✓ should update state_info with PUT
    ✓ should throw an error if you PUT with a wrong id
    ✓ should remove a state from the db with the DELETE mehod

  /api/v1/state_facts
    ✓ should GET all state facts
    ✓ should GET a single state fact by id
    ✓ should throw an error when passed an incorrect state fact id
    ✓ should POST state_facts
    ✓ should throw an error if POST is missing a required parameter
    ✓ should update state_facts with PUT
    ✓ should throw an error if you PUT with a wrong id
    ✓ should remove state facts from the db with the DELETE mehod
  /api/v1/jwt
    ✓ should grant our Turing instructors a JWT
    ✓ should toss them an error when passed incorrect password 


  18 passing (2s)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

/Users/spenserleighton/turing/byob/server.js
   63:12  warning  Identifier 'state_info' is not in camel case   camelcase
   73:12  warning  Identifier 'state_facts' is not in camel case  camelcase
   253:3   error    Unexpected console statement  
   
   the console statement is just the 'running on port 3000' bit...

#### Attach a screenshot of your TravisCI build passing

[Imgur](https://i.imgur.com/GaU0Gv0.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you want to say?

Would love to get some feedback on the two servers done in this mod BEFORE i take the final.

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
