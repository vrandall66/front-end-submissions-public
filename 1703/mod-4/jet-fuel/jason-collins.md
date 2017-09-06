# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/the-oem/jetfuel)

#### Link to the Deployed Application
[heroku](https://fuelthejets.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/the-oem/jetfuel/blob/commented-server/server.js)

## Completion

#### Were you able to complete the base functionality?
Yes, everything as I understand it in the base requirements is completed.

If not, explain what is missing and why.

#### Which extensions, if any, did you complete?
I did not complete any of the extensions.

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/the-oem/jetfuel/blob/master/public/assets/js/script.js#L56)

* Why were you proud of this piece of code?
_~ I wasn't sure what the best way to approach inline sorting of DOM elements would be, so getting this to work in a fairly simple manner felt good. Same could be said for the folder sorting code, as well._

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/the-oem/jetfuel/blob/master/public/assets/js/script.js#L195)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
_~ This is the code to toggle showing and hiding the list of links for a given folder. I did this using jQuery animate(), however I would like to have done something more slick using CSS and just use jQuery to add or remove appropriate classes to the DOM elements. It feels sluggish and choppy using the jQuery code. Sad Panda._

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

![test suite](https://the-oem.github.io/assets/jetfuel-tests.png)

#### Please feel free to ask any other questions or make any other statements below!

* Anything else you wanna say! ~ _It felt pretty good to have the CircleCI tests running with each PR, and seeing the subsequent deploys to Heroku automatically was very cool :)_

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**50 points**: No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use.

## User Interface

**18 points**: The application is logical, and easy to use. There no holes in functionality and the application stands on it own to be used by the instructor without guidance from the developer.

* Some sort of active styling on the Add Folder/Add Link buttons would be nice. I could see these being tabs where the form itself has a background on it that attaches it to these two toggleable tabs.
* CSS Animation is a little rigid at points but I think the vertical slide is a good use case for opening folders.
* Nice input validation/error handling in the UI for invalid URLs and folders.

## Data Persistence with SQL Database

**18 points**: The application persists data in a SQL database but with correct relationships between folders and URLs, slight error with column fields re: uniqueness

* The [shortUrl](https://github.com/the-oem/jetfuel/blob/master/src/server/db/migrations/20170815155033_initial.js#L16) must be a unique value. If you generate two of the same short URLs, that point to different long URLs, one of them will be overridden. 

## Annotated Server File

**10 points**: Each line of the server file (on a separate branch) is commented and explains the code using precise, correct terminology and specificity

## Testing

**18 points**: Project has a running test suite that tests every server-side endpoint with many happy and sad path cases.

* Don't do [rollbacks](https://github.com/the-oem/jetfuel/blob/master/test/integration/routes.spec.js#L18-L20) in your test file. (Also not in an afterEach). You're undoing it by running a migrate latest immediately after anyway, so it's not doing anything. But it's also putting your database out of sync for some amount of time. You only want to be testing on the latest most up-to-date schema and by doing a rollback you are outdating your database.

* I wouldn't necessarily respond with a 404 [here](https://github.com/the-oem/jetfuel/blob/master/test/integration/routes.spec.js#L153-L165) as a folder can exist without links. 404 means the endpoint cannot find a resource to exist at it or the endpoint doesn't exist. When you do a select you actually get back an empty array, which is still *something*. It's not technically an error if a folder doesn't have URLs. This is a good discussion on when to use [404s](https://softwareengineering.stackexchange.com/questions/203492/when-to-use-http-status-code-404-in-an-api)

## JavaScript Style

**15 points**: Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

* Nitpick but I usually group my app.sets separately from my [app.uses](https://github.com/the-oem/jetfuel/blob/master/server.js#L8-L10). When you have a bigger, more complex application the order and organization is more important. 

* You shouldn't really need to set an additional success/error [status](https://github.com/the-oem/jetfuel/blob/master/server.js#L20-L26) because the response will automatically come back with an `ok` flag based on the status code you send it. Doesn't hurt anything, but is a little redundant.

* Some further [validation](https://github.com/the-oem/jetfuel/blob/master/server.js#L33-L35) you could do here is detect if name is the proper data type. What if someone passed in an integer or something weird?

* This [ternary](https://github.com/the-oem/jetfuel/blob/master/server.js#L65-L74) is really difficult to read. Good rule of thumb is to only use ternaries for left-hand assignments that have a binary value and can fit on one line. e.g `var foo = bar ? baz : zam`

* First things first [always use .catch with your promises](https://github.com/the-oem/jetfuel/blob/master/public/assets/js/script.js#L19-L26). Second, you're deferring `apiGetFolders` until the document is ready --- fetch requests are not dependent on the DOM being ready. You should kick this off immediately and only include functions that depend on the DOM in document.ready.

* Without methods, using a [class](https://github.com/the-oem/jetfuel/blob/master/public/assets/js/script.js#L29-L42) here is a bit over-engineered.

* Ahhh, I can't read [this](https://github.com/the-oem/jetfuel/blob/master/public/assets/js/script.js#L54). Don't get too carried away with your terneries and there's no need to squish everything onto one line.

* DOM operations like [appending](https://github.com/the-oem/jetfuel/blob/master/public/assets/js/script.js#L68-L70) are expensive and slow. You want to use [Document Fragments](https://developer.mozilla.org/en-US/docs/Web/API/DocumentFragment) here and build up all the HTML you need to append to the dom in a fragment first, then do a single append when it's all ready.


## Workflow

**16 points**: The developer makes a series of small, atomic commits that document the evolution of their application though some are taking on a bit too much responsibility.

* Nice readme!
* Nice consistently formatted commit messages, though I'm concerned about the low number of commits. I'd expect a project like this to have a least 100; that's how granular and specific your changesets should be. Commits like [this](https://github.com/the-oem/jetfuel/commit/897d17af767053f44b6a66404050b81267bf3f62) are doing a bit too much and more than I'd expect given the commit message.
* Nice use of branches appropriately named
* I would avoid committing TO DO comments - file issues for those things instead or keep those on a branch, and remove them when the branch functionality is complete and you want to merge to master.
* [Ahhhhh](https://github.com/the-oem/jetfuel/blob/master/src/server/db/migrations/20170815155033_initial.js#L23)


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: 145 / 160
