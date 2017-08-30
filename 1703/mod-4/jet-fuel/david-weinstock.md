# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/dstock48/jet-fuel)

#### Link to the Deployed Application
[heroku](https://jet-fuel-8888.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/dstock48/jet-fuel/blob/comments/server.js)

## Completion

#### Were you able to complete the base functionality?

Yes.

#### Which extensions, if any, did you complete?

None.

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/dstock48/jet-fuel/blob/76cdd8e3dac9f394386742d60196ae1696b50035/public/main.js#L123-L144)

* Why were you proud of this piece of code?

I thought this was a pretty nifty way of dynamically creating div containers with a classname corresponding to the folder name passed into the function. And then using that classname to be dynamically targeted in the next function to add link cards to their corresponding container.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/dstock48/jet-fuel/blob/76cdd8e3dac9f394386742d60196ae1696b50035/public/main.js#L96-L111)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

This felt like a very hacky way of getting the fontawesome folder icon to toggle between open/close. I wish there could have been a more simple way to just toggle a single class on and off that would have switched between the open/close icon.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
npm test

> jet-fuel@1.0.0 test /Users/Dave/Documents/Turing/MOD4/projects/jet-fuel
> mocha



Jet Fuel URL Shortener is running on http://localhost:8888
  Client-side Routes
    ✓ should return the static HTML file
    ✓ should redirect from a shortened URL to a long URL (648ms)

  API Routes
    GET /api/v1/folders
Re-seed complete!
      ✓ should return all of the folders
Re-seed complete!
      ✓ should return an error status if you do not hit the correct endpoint
    POST /api/v1/folders
Re-seed complete!
      ✓ should create a new folder
Re-seed complete!
      ✓ should not create a new folder with missing data
Re-seed complete!
      ✓ should not create a folder with a duplicate name
    GET /api/v1/links
Re-seed complete!
      ✓ should return all of the links
Re-seed complete!
      ✓ should return an error status if you do not hit the correct endpoint
    POST /api/v1/links
Re-seed complete!
      ✓ should create a new link
Re-seed complete!
      ✓ should not create a new link with missing data


  11 passing (1s)
```

#### Please feel free to ask any other questions or make any other statements below!

This was a fun project! It was definitely a lot of new concepts to learn in a week, but it really helped demystify what goes on in the back-end.

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**40 points**:

* Bug: When you open the page, the link folders are open, but they do not show any links within them even after you close and open the folders again - this seems to be a sporadic bug. Refresh a few times and you see different behaviors.

## User Interface

**20 points**:

* So bright! But I like the general layout. Very easy to use and the copied shortened link is a nice additional feature.

## Data Persistence with SQL Database

**20 points**:

* Keep in mind that `Promise.all` will not guarantee the order or which promises [in the array](https://github.com/dstock48/jet-fuel/blob/master/db/migrations/20170816133314_initial.js#L3) are resolved. The code in the array will be started int he order of the indices, 
but the resolution of the promises will not necessarily be in the same order. This could be an issue if the code in one promise relies and the code in another promise that assumes a particular order.
* Good idea for a [database validation](https://github.com/dstock48/jet-fuel/blob/master/db/migrations/20170816133314_initial.js#L8)

## Testing

**15 points**:

* I would consider taking out the "Reseed complete" console.log - this kind of hurts readability of your test suite in the terminal, and once you know you're hooks are working, then you can be confident about your reseed.
* Would like to see a sad path test for if a shortened URL does not exist [here](https://github.com/dstock48/jet-fuel/blob/master/test/routes.spec.js#L57)
* The 404 tests for the "folders" and "links" are really the same test because they test Express's default 404 handler. Express just doesn't find a route with that spelling, so it throws a 404.
* Good overall happy and sad path tests

## Commented Server File

**10 points**: Good comments

## JavaScript Style

**15 points**:

* I'm guessing the reason why there are sometimes links in folders and sometimes not is the progression of this [fetch call](https://github.com/dstock48/jet-fuel/blob/master/public/main.js#L166-L178). 
If the link container is not ready for appending, then maybe nothing is appended to it. In this sequence, you want to make sure the folders and link containers are available before you try to append things withing the fetch call. Async is fun.
* I think ideally you wouldn't want to change the ascending/descending links by making a request, reloading the page, and putting everything on the DOM again - I think this would mainly be done client side without going to the database again.
* Make sure you are using `.catch()` on [every promise](https://github.com/dstock48/jet-fuel/blob/master/server.js#L30)
* [This](https://github.com/dstock48/jet-fuel/blob/master/server.js#L60-L61) is OK to use here, but when you have a lot of route tied to that endpoint, readability will suffer a lot as more HTTP methods are added

## Workflow

**20 points**: Good job using a gitignore


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: 140 / 160
