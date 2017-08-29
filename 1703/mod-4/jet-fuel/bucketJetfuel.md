# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/danielbucket/JetFuel)

#### Link to the Deployed Application
[heroku](https://jetgas.herokuapp.com/)

#### Link to your annotated server file
[annotated server file]()

## Completion

#### Were you able to complete the base functionality?

If not, explain what is missing and why.
* Didn't get the sorting done. Short on time.
* URL validation. Short on time.
* Date display. Short on time.
* Testing using seeding. Short on time.

#### Which extensions, if any, did you complete?

# Code Quality

  * I'd be proud of my code if I felt like I was able to really put time and care into making something significant. As it is, all my code was written rushed and haphazard.

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
* Time is the number one challenge. When you spend 3/7 days trying to remember how to write jQuery and another 2 days troubleshooting, you're left with 2 days of actual code writing.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

`
Server is running on 3300
  Client Routes
    ✓ should return status(200) (44ms)
    ✓ sad panda path

  GET/api/v1/folders
    ✓ should return

  GET/api/v1/shortURL
    ✓ should return these values:


  4 passing (100ms)

danielbucket:jetfuel/ (master) $
`

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Robbie)

## Specification Adherence

<!-- **50 points**: -->

* App not yet functioning on production

## User Interface

<!-- **20 points**: -->

* App not yet functioning on production

## Data Persistence with SQL Database

**20 points**:

* Schema looks good - good database validation for unique [folder names](https://github.com/danielbucket/JetFuel/blob/master/db/migrations/20170816132459_initial.js#L6)
* Keep in mind that `Promise.all` will not guarantee the order or which promises [in the array](https://github.com/danielbucket/JetFuel/blob/master/db/migrations/20170816132459_initial.js#L3) are resolved. The code in the array will be started int he order of the indices, 
but the resolution of the promises will not necessarily be in the same order. This could be an issue if the code in one promise relies and the code in another promise that assumes a particular order.

## Testing

<!-- **20 points**: -->

* Why default to the development environment [here](https://github.com/danielbucket/JetFuel/blob/master/test/serverTest.spec.js#L6) - you always want your tests to run with the `test` environment
* In your [beforeEach hook](https://github.com/danielbucket/JetFuel/blob/master/test/serverTest.spec.js#L34-L38) - good job with seeding data before each test, but you only want to run the migrations once before ALL tests in the file - 
so for the migrations you can use the `before` test hook

* Most tests are commented out at this point

## Commented Server File

**5 points**: Good high-level comments, but need more details comments about nearly every line of code (and on a separate branch)

## JavaScript Style

**15 points**:

* Consider using document fragments [here](https://github.com/danielbucket/JetFuel/blob/master/public/scripts.js#L31) for appending items to the DOM, which will be more efficient for larger numbers of links or folders
* Careful with the [`console.log`](https://github.com/danielbucket/JetFuel/blob/master/public/scripts.js#L65)
* By the name of [this function](https://github.com/danielbucket/JetFuel/blob/master/public/scripts.js#L97), I would imagine that it does a fetch call to get all of the folders from the database, but it looks like you're using the POST function inside of it
* Another naming nit pick - [this function](https://github.com/danielbucket/JetFuel/blob/master/public/scripts.js#L118) is not clearing inputs, but rather enabling/disabling buttons
* [This route](https://github.com/danielbucket/JetFuel/blob/master/server/server.js#L33) seems like it should be done through error handling in the POST route for a new folder

## Workflow

**15 points**: 

* Be sure not to commit node_modules in your repos - add a gitignore file right away as part of your first commit before your really write any feature code
* Brittany and I really want you to be more vigilant about asking us questions - as soon as you notice that you're really stuck, going down a rabbit hole, or throwing stuff at the wall, 
then let us know


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: x / 160


**Need to fix before eval can be completed**

* Production is not working - one big reason for this is that your `baseRoute` is defined on your client side using `localhost`, which is not the URL of your heroku app, which is why you're getting a 404 response for POST to `/folders` in the console
  * Instead of using an absolute path with `localhost:3000`, use relative paths in your fetch calls. For instance, instead of the absolute path to `localhost:3000/api/v1/folders`, just use the relative path `/api/v1/folders`

* You need to have s separate branch where you have commented lines explaining your sever file (as described in the project spec)