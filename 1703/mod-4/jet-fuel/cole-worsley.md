# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/coleworsley/jet-fuel)

#### Link to the Deployed Application
[heroku](https://cw-jetfuel.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/coleworsley/jet-fuel/blob/cw-annotated-server/server.js)

## Completion

#### Were you able to complete the base functionality?

Yes

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/coleworsley/jet-fuel/blob/master/db/test/seeds/testSeeds.js#L55-L60)

I was particularly proud of this piece of code as it greatly simplified the idea of importing seeds into a database. By rewriting the code from the lesson in my own style, I was able to gain a much better understanding of the purpose of seeding databases especially for testing

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/coleworsley/jet-fuel/blob/master/public/index.js#L67-L83)

Based on the way I set up my elements, I had to make a couple nasty jquery functions that became hard to follow. I think going forward, I want to do my best to create more modularized code.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://github.com/coleworsley/jet-fuel/blob/master/public/assets/images/testsuite.png)

#### Please feel free to ask any other questions or make any other statements below!

Fun project! Everything was pretty straightforward and clearly explained. It was definitely weird working with jQuery after using react for so long!

-----

# Instructor Feedback (Robbie)

## Specification Adherence

**40 points**:

* Do not see link sorting functionality
* No URL validation

## User Interface

**15 points**:

* The UI is pretty pleasant to use - I would add a title/description to the links or else I don't know what they represent or where they will go
* The form labels/place holders are difficult to read

## Data Persistence with SQL Database

**20 points**:

* Good database validation for unique [folder names](https://github.com/coleworsley/jet-fuel/blob/master/db/migrations/20170815172451_initial.js#L6)
* Keep in mind that `Promise.all` will not guarantee the order or which promises [in the array](https://github.com/coleworsley/jet-fuel/blob/master/db/migrations/20170815172451_initial.js#L3) are resolved. The code in the array will be started int he order of the indices, 
but the resolution of the promises will not necessarily be in the same order. This could be an issue if the code in one promise relies and the code in another promise that assumes a particular order.
* Be sure to use a `catch()` for [all promises](https://github.com/coleworsley/jet-fuel/blob/master/db/seeds/dev/folders.js#L53)

## Testing

**15 points**:

* You should be relying on the primary key auto increment in [your actual test](https://github.com/coleworsley/jet-fuel/blob/master/test/routes.spec.js#L58) instead of supplying an ID, a user wouldn't (shouldn't) send an ID through in the API request
* Would like to see a sad path test [here](https://github.com/coleworsley/jet-fuel/blob/master/test/routes.spec.js#L188) for the case where a shortened URL does not exist in the DB

## Commented Server File

**8 points**: Good comments, looking for a bit more detail on dependencies and middleware

## JavaScript Style

**15 points**:

* When using `fetch`, the `catch()` will not be thrown if the [fetch call](https://github.com/coleworsley/jet-fuel/blob/master/public/index.js#L4) receives a 404 response - it only goes to the catch if there are network errors. 
So you should check for `response.ok`
* Instead of using the id attribute in an element to store information like the [folder id value](https://github.com/coleworsley/jet-fuel/blob/master/public/index.js#L13), consider using the data attribute which is actually used for holding data values
* Break out your fetch calls into separate functions since you might reuse the same call
* The form of [this params check](https://github.com/coleworsley/jet-fuel/blob/master/server.js#L35-L39) is the same with a couple routes - could be made into its own function of even custom middleware

## Workflow

**15 points**:

* What is this readme file? (https://github.com/coleworsley/jet-fuel/blob/master/README.md)
* Be sure not to include node_modules right off the bat. If you commit them even once, they'll be in the git version history of your project.


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: 128 / 160
