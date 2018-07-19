# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/CharlesY712/BYOB)

#### Link to the Deployed Application
[Heroku](https://super-fun-backend.herokuapp.com/)


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

* Setup automatic deployments with TravisCI to a production app on Heroku?
(Yes)

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/CharlesY712/BYOB/blob/d86a9cf1019308855f8190f6711b366fef135839/server.js#L44-L68)

* Why were you proud of this piece of code?

Having never made a query request before, we used the documentation and were able to get it working on our first attempt.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code]()

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

We had absolutely zero css for this project. Having gone through 6 months of Front-End program only to not style felt not awesome. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

      Endpoint tests      
    ✓ should GET all the states      
    ✓ should query station search      
    ✓ should GET one state        
    ✓ should GET all the cities        
    ✓ should GET one city        
    ✓ should POST a new token with admin set to true        
    ✓ should POST a different token with admin set to false        
    ✓ should THROW a 404 ERROR when missing params        
    ✓ should POST a new state        
    ✓ should ERROR when missing a state param        
    ✓ should POST a new city        
    ✓ should ERROR if missing a cities param        
    ✓ should PATCH a state in states DB if it has state in body        
    ✓ should PATCH a state in DB if numberOfStations is in body        
    ✓ should not PATCH a state in states DB if incorrect ID        
    ✓ should not PATCH a state DB if missing body information        
    ✓ should PATCH a city in cities DB if it has city in body        
    ✓ should PATCH a city in cities DB if it has BD in body        
    ✓ should PATCH a city in cities DB if it has CNG in body        
    ✓ should PATCH a city in cities DB if it has E85 in body        
    ✓ should PATCH a city in cities DB if it has ELEC in body        
    ✓ should PATCH a city in cities DB if it has HY in body        
    ✓ should PATCH a city in cities DB if it has LNG in body        
    ✓ should PATCH a city in cities DB if it has LPG in body        
    ✓ should not PATCH a city in cities DB if incorrect ID        
    ✓ should not PATCH a city in cities DB if missing body        
    ✓ should DELETE state from states DB        
    ✓ should not DELETE state from states DB when wrong ID is sent        
    ✓ should not DELETE state from states DB no ID is sent        
    ✓ should DELETE a city from cities DB        
    ✓ should not DELETE city from cities DB when wrong ID is sent        


  31 passing (3s)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

~/turing/mod4/BYOB [master] $ npm run eslint

> byob@1.0.0 eslint /Users/charles/Turing/mod4/BYOB
> ./node_modules/eslint/bin/eslint.js ./*.js ./db/**/*.js ./test/*.js

~/turing/mod4/BYOB [linting2] $ 

#### Attach a screenshot of your TravisCI build passing

[Travis CI](https://cl.ly/2D2I0Q432g3D)

[![Build Status](https://travis-ci.org/CharlesY712/BYOB.svg?branch=master)](https://travis-ci.org/CharlesY712/BYOB)

-----

#### Please feel free to ask any other questions or make any other statements below!

Maddy is a rock star and the other two are delenquints... 

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