# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/buji405/jet-fuel)

#### Link to the Deployed Application
[heroku](https://ciaras-jetfuel.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/buji405/jet-fuel/blob/0a0fa18239f2247b0140f385fb6c11120b26c690/backend/server.js)

## Completion

#### Were you able to complete the base functionality?

If not, explain what is missing and why.

Yes, there is a known bug though with validating the url. 
If I add a invalid link it will append it to the dom as undefined, but if you refresh 
it goes away and never adds to the database. I looked a hundred times at why the catch 
isn't blocking it from appending but can't figure it out. Everything seems to be in place. 

Also I did add a delete method which wasn't required but it only deletes the folders if there is nothing in them. 

#### Which extensions, if any, did you complete?
didn't get that far

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code]()
$(e.target).parent().find(".drop-down").toggleClass("show") 
$('.info-wrapper').empty()

* Why were you proud of this piece of code?
because it took me forever to target this and get the toggle going. was exciting when it finally worked! 
Also the second line because I had a problem for a long time where every time I clicked the folder it was 
duplicating all the links, took a long time to figure out what I needed to clean to get it to not duplicate. 

#### Link to a specific block of your code on Github that you feel not great about
[sad code]()
appendInfo(res.origURL, res.description, parentElement, res.shortURL, res.id, res.created_at)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
I don't like all the things I'm having to pass through. I think I could have just passed res and parent element 
but when I tried doing this it was breaking everywhere so I think I just would need more time to figure out all the 
places to change everything. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()
<img width="1038" alt="screen shot 2017-08-20 at 10 31 41 pm" src="https://user-images.githubusercontent.com/18603030/29503701-74be8d74-85f7-11e7-867d-6301ae206630.png">

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**40 points**:

* Minor bug: If you open a folder, it expands the links, but when you click on a second folder, the first folder's links are hidden and shows only the form.
* Sorting links in ascending or descending order does not seem to work on production
* Delete for the folder was not required for the spec, but cool that you added it

## User Interface

**15 points**:

* I think it's interesting that the form is under each folder. At first, I didn't know how to submit a link to be shortened, which is a minor UX issue, but then I found out to create a folder first and explore.
* The sort by ascending/descending order is not labeled for what is being ordered

## Data Persistence with SQL Database

**20 points**: Good database validation [here](https://github.com/buji405/jet-fuel/blob/master/backend/db/migrations/20170816164222_initial.js#L6) for unique folder names

## Testing

**15 points**:

* You are setting the node environment on the first line [here](https://github.com/buji405/jet-fuel/blob/master/backend/test/routes.spec.js#L1-L3), there is no need for the `||` (the OR will never be hit)
* In this `beforeEach()` [here](https://github.com/buji405/jet-fuel/blob/master/backend/test/routes.spec.js#L28-L39), you are doing too much. You only need to re-seed data before every test. 
For the migration, you want to run it only once in a `before()` hook, not `beforeEach()`. This is because the database schema won't change from test to test, but the records in the database will.
* [This test](https://github.com/buji405/jet-fuel/blob/master/backend/test/routes.spec.js#L56-L64) and [this test](https://github.com/buji405/jet-fuel/blob/master/backend/test/routes.spec.js#L101-L109) are really testing the same thing, which is Express's built-in 404 route handler - spelling folders
incorrectly isn't really testing the "folders" path. Express is looking for a route called `/foldr`, which it will not find defined in your server file, and it will default to a 404, but this has nothing to do with the real "folders" path. 
The same goes for "linx"
* Should be testing more about the content of the response [here](https://github.com/buji405/jet-fuel/blob/master/backend/test/routes.spec.js#L122)
* A good test [here](https://github.com/buji405/jet-fuel/blob/master/backend/test/routes.spec.js#L151-L158), but doesn't belong with the group of POST requests if you're grouping by HTTP method
* Overall, pretty good sad path tests

## Commented Server File

**8 points**: Good commenting - would want to see some more detail for at least one specific route handler

## JavaScript Style

**15 points**:

* URL validation should happen client-side so you can stop a bad URL from being sent to your sever. So it's good that you're using the URL validation npm package, 
but if it's in the server, then you won't know the URL is bad until it gets to the server.
* After a folder has been created and you have a successful response, then you can create the folder client side and do not need to make another [request](https://github.com/buji405/jet-fuel/blob/master/backend/public/main.js#L51) here for all of the folders again. 
Just make the POST request, and on success of that, append it to the DOM without the request for all folders to reduce the number of requests since these take a relatively long time
* Good job using `catch()` for all of your fetch promises
* Why a status of 501 [here](https://github.com/buji405/jet-fuel/blob/master/backend/server.js#L66) instead of a 500?
* Why the difference using `app.route` [here](https://github.com/buji405/jet-fuel/blob/master/backend/server.js#L102) instead of `app.get`? Also, there should be error handling for if 
a shortened link is not found. Right now, the `catch` will only be gotten to if there is a server/database error. If something is not found in the database, it will 
not necessarily error, but instead return an empty array.

## Workflow

**15 points**: Do not commit node_modules - always git ignore!


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: 128 / 160
