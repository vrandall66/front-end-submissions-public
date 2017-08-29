# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/Ggoering/Jet-Fuel)

#### Link to the Deployed Application
[heroku](https://gg-jet-fuel-winning.herokuapp.com/)

#### Link to the annotated server file
[annotated server file 1](https://github.com/Ggoering/Jet-Fuel/blob/master/server.js)
[annotated server file 2](https://github.com/Ggoering/Jet-Fuel/blob/master/routes.js)
[annotated server file 3](https://github.com/Ggoering/Jet-Fuel/blob/master/controller.js)

## Completion

#### Were you able to complete the base functionality?

Everything except CSS animation

I built the drop downs and box displays using a display: none toggle.  Apparently you can't do CSS transitions with that CSS property.  Had my 1 yr wedding anniversary so spent a lot of this weekend doing non-coding things and couldn't learn a new way to implement & refactor in time for submission.

#### Which extensions, if any, did you complete?

None

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/Ggoering/Jet-Fuel/blob/master/public/scripts.js#L7-L9)

* Cool UX I copied from bit.ly and I have no idea why I needed to do the setTimeout to have access to the pasted element (without the setTimeout event.target.value and the val() of the input field were undefined or empty string) but it was my idea to try it and it worked.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/Ggoering/Jet-Fuel/blob/master/public/scripts.js#L52-L75)

* I am having to clear the input fields before applying the for loop because I don't know how to append without duplicating what was there already & still reuse this same function everywhere possible. It wouldn't be so bad but it makes it so that the expanded folder tabs have to be reopened which is bad UX.  I'd probably hunt around for a better jQuery method than .append in order to refactor.

* In general all my event listeners are a little sad because I didn't get to implement button disables, key code refusals, and displaying of error messages to the user if they didn't submit something properly.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()

Jet Fuel is running on 3000.
  Client Route
    ✓ is a single page app (43ms)
    ✓ should return a 404 for a route that does not exist

  API routes
    GET /api/v1/link
      ✓ Should return a list of all the links
    POST /api/v1/link
      ✓ should add a new link
    PUT /api/v1/link/:id
      ✓ should update a link with folder and description
    GET /api/v1/folder
      ✓ should list all the folders
    POST /api/v1/folder
      ✓ should add a new folder


  7 passing (356ms)


#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Robbie)

## Specification Adherence

<!-- **50 points**: -->

* I have no idea how to add a folder or add a link to a folder (is this broken?)
* Don't see a way to sort links in ascending/descending order

## User Interface

**10 points**:

* The way that the links span the entire page is rough, and the text is very small
* Folder names are all the way over to the left of the page even though the names are very short

## Data Persistence with SQL Database

**20 points**:

* Good database validation for unique [folder names](https://github.com/Ggoering/Jet-Fuel/blob/master/db/migrations/20170815195822_initial.js#L6)
* Keep in mind that `Promise.all` will not guarantee the order or which promises [in the array](https://github.com/Ggoering/Jet-Fuel/blob/master/db/migrations/20170815195822_initial.js#L3) are resolved. The code in the array will be started int he order of the indices, 
but the resolution of the promises will not necessarily be in the same order. This could be an issue if the code in one promise relies and the code in another promise that assumes a particular order.

## Testing

**10 points**:

* Good job with the minimal and appropriate test hooks (beforeEach and before)
* [This line](https://github.com/Ggoering/Jet-Fuel/blob/master/test/routes.spec.js#L1) could just be `const environment = process.env.NODE_ENV || 'test';`
* Need more sad paths for a shortened URL that doesn't exist and for POST requests with missing body information

## Commented Server File

**8 points**: Good comments, but these should be on a separate branch, not `master`

## JavaScript Style

**15 points**:

* Why do you have [this PUT](https://github.com/Ggoering/Jet-Fuel/blob/master/routes.js#L16) functionality - it wasn't part of the spec and time could have been spent elsewhere
* Nice use of the Express Router to extract some code
* The controller file is a little overkill for this project, and normally there are separate controllers for each model (folders and links would each have a separate controller)
* The [resource routes](https://github.com/Ggoering/Jet-Fuel/blob/master/routes.js#L10) should be plural according to the RESTful API conventions - `api/v1/links` and `api/v1/folders`
* If no links are found [here](https://github.com/Ggoering/Jet-Fuel/blob/master/controller.js#L21), then knex will return an empty array, not an error
* Be sure to use a `catch()` on [every promise](https://github.com/Ggoering/Jet-Fuel/blob/master/public/scripts.js#L52) for error handling, including fetch calls
* Consider using document fragments [here](https://github.com/Ggoering/Jet-Fuel/blob/master/public/scripts.js#L64) for appending items to the DOM, which will be more efficient for larger numbers of links or folders

## Workflow

**10 points**:

* Committing `DS_Store` and `node_modules` is a problem, especially if you just leave them in your repo
* Huge initial commits - need to break these down so you have a good way to track changes - if something goes wrong you know what commit (and small changes) to pinpoint it to


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: x / 160
