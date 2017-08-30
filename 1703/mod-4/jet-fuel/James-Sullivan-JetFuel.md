# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project

[jetfuel](http://frontend.turing.io/projects/jet-fuel.html)

#### Link to the Deployed Application

[heroku](https://jtfule.herokuapp.com/)

#### Link to your annotated server file

[annotated server file](https://gist.github.com/jsullivan5/79cdcb95e6a3095bcc8f8b495b0d4c2a)

## Completion

No.

If not, explain what is missing and why.

I completed everything but the CSS transition. I finished this really late Sunday night and could not figure out how to debug
the issues in time. See sad code below.

None

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/jsullivan5/jet-fuel/blob/master/public/scripts.js#L159)

This is just reordering the cards with jQuery.  But it took me a long time to arrive at this.  I like it because I was able to
impliment it without any server side code, which I initially thought I would need to do.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/jsullivan5/jet-fuel/blob/master/public/styles.css#L115)

This was the CSS transition I could not figure out at 3:00 AM.  I thought it would be simpler to do.  My app has a get request 
every time the folder changes and renders.  My understanding is that adding a class can be trickier when a component is rendering
and there are default browser optimizations to consider.  I wish I would have gotten this to work.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
Jet Fuel is running on http://localhost:3000.
  Client Routes
    ✓ should return the home page
    ✓ should return a 404 if endpoint not found

  API Routes
    GET /api/v1/folders
done seeding
done seeding
      ✓ should get the folders
    POST /api/v1/folders
done seeding
done seeding
[ anonymous { name: 'beers', id: 3 } ]
      ✓ should create a new folder (40ms)
done seeding
done seeding
[ anonymous { name: 'beers', id: 3 } ]
      ✓ should return an error if user tries to duplicate folder.
done seeding
done seeding
      ✓ should return 422 if insufficient data is provided
    GET api/v1/folders/:id/links
done seeding
done seeding
      ✓ should get links for a folder
    POST /api/v1/links
done seeding
done seeding
{ long_URL: 'http://www.expedia.com',
  short_URL: 'http://jt.fl/ca2ea3b5',
  folder_id: 1,
  description: 'expedia' }
      ✓ should create a link
done seeding
done seeding
{ long_URL: 'http://www.expedia.com',
  short_URL: 'http://jt.fl/ca2ea3b5',
  folder_id: 1 }
      ✓ should return 422 if insufficient data is provided
    GET /api/*/:charHash
done seeding
done seeding
      ✓ should accept GET request to redirect (225ms)
```


  10 passing (1s)

#### Please feel free to ask any other questions or make any other statements below!

It was a fun project. I really enjoyed working in the back and and have some ideas on how I need to level up on these skills.

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**40 points**:

* No animation showing the opening or closing of folders - everything is done through selecting through the drop down instead...
* Bug: I can try to ad a link while "Select a Folder" is selected in the drop down, and the link goes through as `undefined` (when you refresh, it disappears)
* Good client-side URL validation

## User Interface

**15 points**:

* The form is a little rough to get through
* I wish I could see what folder I'm on other than viewing it through the tiny drop down menu

## Data Persistence with SQL Database

**20 points**:

* Keep in mind that `Promise.all` will not guarantee the order or which promises [in the array](https://github.com/jsullivan5/jet-fuel/blob/master/db/migrations/20170816133440_initial.js#L3) are resolved. The code in the array will be started int he order of the indices, 
but the resolution of the promises will not necessarily be in the same order. This could be an issue if the code in one promise relies and the code in another promise that assumes a particular order.
* Good database validation for [unique folder names](https://github.com/jsullivan5/jet-fuel/blob/master/db/migrations/20170816133440_initial.js#L6)

## Testing

**15 points**:

* Why separate lines [here](https://github.com/jsullivan5/jet-fuel/blob/master/test/routes.spec.js#L3-L4)?
* [This](https://github.com/jsullivan5/jet-fuel/blob/master/test/routes.spec.js#L39-L50) is too much to be doing in this kind of hook. You only need to re-seed data before every test. 
For the migration, you want to run it only once in a `before()` hook, not `beforeEach()`. This is because the database schema won't change from test to test, but the records in the database will.
* Good sad path test [here](https://github.com/jsullivan5/jet-fuel/blob/master/test/routes.spec.js#L106-L125)
* Would like to see a sad path test [here](https://github.com/jsullivan5/jet-fuel/blob/master/test/routes.spec.js#L248) for the case where a shortened URL does not exist in the DB

## Commented Server File

**10 points**: Good commented server file

## JavaScript Style

**15 points**:

* Nice use of the Express Router to extract some code
* The controller file is a little overkill for this project, and normally there are separate controllers for each model (folders and links would each have a separate controller)
* Would extract [this fetch call](https://github.com/jsullivan5/jet-fuel/blob/master/public/scripts.js#L3-L5) to it's own function
* Consider using document fragments [here](https://github.com/jsullivan5/jet-fuel/blob/master/public/scripts.js#L20-L24) for appending items to the DOM, which will be more efficient for larger numbers of links or folders
* Be sure to use a `catch()` on [every promise](https://github.com/jsullivan5/jet-fuel/blob/master/public/scripts.js#L6) for error handling, including fetch calls
* When using `fetch`, the `catch()` will not be thrown if the [fetch call](https://github.com/jsullivan5/jet-fuel/blob/master/public/scripts.js#L90) receives a 404 response - it only goes to the catch if there are network errors. 
So you should check for `response.ok`
* You tend to have a lot of [whitespace](https://github.com/jsullivan5/jet-fuel/blob/master/public/scripts.js#L131) in your JS. Is this for your own readability? You could probably cut down on it if the function is only two lines of code within it.
* [This is brutal](https://github.com/jsullivan5/jet-fuel/blob/master/public/scripts.js#L166) to read - definitely break this out into more readable logic, no sense in being clever with a one liner that is really hard to read and debug.
* Careful with the [`console.log`](https://github.com/jsullivan5/jet-fuel/blob/master/server/controller.js#L30)
* [These](https://github.com/jsullivan5/jet-fuel/blob/master/server/controller.js#L59-L65) are fairly repetitive in other routes, I imagine you could extract them into their own function and pass in the required params (or even write your own middleware)

## Workflow

**15 points**: Be sure not to include node_modules right off the bat. If you commit them even once, they'll be in the git version history of your project.


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: 130 / 160
