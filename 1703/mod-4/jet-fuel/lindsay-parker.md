# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/lindsaywparker/jet-fuel)

#### Link to the Deployed Application
[heroku](http://lwp-jetfuel.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/lindsaywparker/jet-fuel/blob/master/server-annotated.js)

## Completion

#### Were you able to complete the base functionality?

Yes

#### Which extensions, if any, did you complete?

None

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/lindsaywparker/jet-fuel/blob/master/public/scripts.js#L62-L64)

* I'm proud of this piece of code because it's a clean refactor that allows for easily communicating various messages to the user.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/lindsaywparker/jet-fuel/blob/master/public/scripts.js#L41-L50)

* I don't feel awesome about this code because the way it's currently written sorts all links instead of the links only in the current folder.  The challenge in refactoring this code was limited time.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://github.com/lindsaywparker/jet-fuel/blob/master/test-results.png)

#### Please feel free to ask any other questions or make any other statements below!

* Jet Fuel was an interesting project, mostly enjoyable.  Working in jQuery again was a fun challenge.

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**50 points**: No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use.

## User Interface

**20 points**: The application is pleasant, logical, and easy to use. There no holes in functionality and the application stands on it own to be used by the instructor without guidance from the developer.

* Nice user messaging on successful creation of a new folder/url.
* CSS animation on expanding a folder is a little bizarre, we didn't set any hard requirements on it but from a UI perspective I'd imagine a vertical slide down for the URls rather than a horizontal shift in the data.

## Data Persistence with SQL Database

**18 points**: The application persists data in a SQL database but with correct relationships between folders and URLs, slight error with column fields re: uniqueness

* This short url [here](https://github.com/lindsaywparker/jet-fuel/blob/master/db/migrations/20170816133448_initial.js#L14-L15) is actually the field that needs to be unique, not the long url. You can create as many short links to `https://www.google.com` as you want and place them in as many folders as you want, but they should each have their own unique short url.

## Testing

**20 points**: Project has a running test suite that tests every server-side endpoint with many happy and sad path cases.

* I'd rather see you set this [environment](https://github.com/lindsaywparker/jet-fuel/blob/master/test/routes.spec.js#L6) variable in your test running script in your package.json rather than hardcoding it here

* Still good to have .catches [here](https://github.com/lindsaywparker/jet-fuel/blob/master/test/routes.spec.js#L33-L38) in case there is something wrong with your test seed data

* I'm surprised if [this](https://github.com/lindsaywparker/jet-fuel/blob/master/test/routes.spec.js#L50-L53) is consistently passing? There is no gaurantee your data will come back in a sorted order so these folder names could come back in different spots in the array.

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**15 points**: The developer makes a series of small, atomic commits that document the evolution of their application. There are some formatting issues in the code base.

* Great use of branches informatively named
* Nice consistently formatted commit messages though [some of them](https://github.com/lindsaywparker/jet-fuel/commit/7199a9877995cc89a017a56923342a85b2c83858) aren't super informative and contain some instances of commented out code. 

### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: x / 150
