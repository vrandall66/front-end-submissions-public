# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/JustynaField/jet-fuel)

#### Link to the Deployed Application
[heroku](https://justyna-jet-fuel.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/JustynaField/jet-fuel/blob/master/server-comments.js)

## Completion

#### Were you able to complete the base functionality?

I have all of the base functionality working, except for these two pieces:

- Visit a folder and sort the folder’s URLs by how recently they were added (both descending and ascending order)
- Enter a URL to be shortened only if it is a valid URL (impose some kind of URL validation)

I ran out of time, also, I found these last two things a little complex and time-consuming.

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[server.js](https://github.com/JustynaField/jet-fuel/blob/master/server.js),
[test seeds](https://github.com/JustynaField/jet-fuel/blob/master/db/test/seeds/folders.js)

* Why were you proud of this piece of code?

It is the first time that I built back-end code and it makes me feel really good. 

#### Link to a specific block of your code on Github that you feel not great about
* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I do not feel awesome about not completing the sorting function. It was harder than I thought it would be. jQuery ''bubbling' made it difficult to create events on elements inside folders. 
I tried url validation by either using regex, or npm package, and could not make it to work.
Also, the heroku page does not represent the most up-to-date version of my app. I didn't know how to update my app on heroku.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
  Client Routes
    ✓ Should return homepage (47ms)
    ✓ should return a 404 for a route that does not exist

  API Routes
    GET /api/v1/folders
      ✓ should return all of the folders
    GET /api/v1/folders/:id
      - should return folder by id
      ✓ should return an error if a requested folder does not exist
    POST /api/v1/folders
      ✓ should create a new folder (40ms)
      ✓ should not create a record with missing data
    GET /api/v1/links
      ✓ should return all of the links
    POST /api/v1/links
      ✓ should post a new link
      - should not create link if required data is missing
    GET /api/v1/folders/:id/links
      ✓ should return links belonging to a specific folder
      - should not return links for folrder that does not exist


  9 passing (828ms)
  3 pending
```


#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**40 points**: There is one feature missing from the base expectations that make the application feel incomplete or hard to use.

## User Interface

**18 points**: The application is pleasant, logical, and easy to use. There no holes in functionality and the application stands on it own to be used by the instructor without guidance from the developer.

* CSS transition is a little rigid when opening or closing a folder. I'd also like the cursor to turn into a 'hand' like a regular clickable link when I hover on one of the folders so that there's a more clear indication that I can click on this thing to expand or collapse it.

## Data Persistence with SQL Database

**18 points**: The application persists data in a SQL database but with correct relationships between folders and URLs, slight error with column fields re: uniqueness

* The [shortUrl](https://github.com/JustynaField/jet-fuel/blob/master/db/migrations/20170816132247_initial.js#L14) must be a unique value. If you generate two of the same short URLs, that point to different long URLs, one of them will be overridden. 
 
## Annotated Server File

**8 points**: Each line of the server file (on a separate branch) is commented and explains the code using mostly accurate terminology

* [Note also that it's falling back to running on port 3000, not that it is always running on 3000](https://github.com/JustynaField/jet-fuel/blob/master/server-comments.js#L21)
* [What does a POST request actually do? I'd like to know that you recognize that it creates a new resource](https://github.com/JustynaField/jet-fuel/blob/master/server-comments.js#L53-L54)
* I wouldn't call id a [placeholder](https://github.com/JustynaField/jet-fuel/blob/master/server-comments.js#L81) here, it represents a 'dynamic segment' of the URL


## Testing

**15 points**: Project has a running test suite that covers most happy and sad paths, though there are some skipped due to errors with seeding.

* I'd rather you set this environment variable in your package.json rather than your [test file](https://github.com/JustynaField/jet-fuel/blob/master/test/server.spec.js#L1)

* We don't need or want to do migration [rollbacks](https://github.com/JustynaField/jet-fuel/blob/master/test/server.spec.js#L39) in our test file because it will manipulate the status of our database schema, and we always want to be testing against the latest most up-to-date schema. I understand the blog post we linked you all to probably led you in this direction, and that's something we'll fix for the next cohort. No points off for this, just wanted to point it out.

* You have a lot of seed files and directories within your repo with inconsistent naming conventions (db/seeds/dev vs. db/test/seeds vs. seed/file-names), it makes it difficult to tell what you're actually seeding your test database with.

* This [test](https://github.com/JustynaField/jet-fuel/blob/master/test/server.spec.js#L70-L77) likely isn't working because you aren't hard-coding the IDs of your folders in your test seed data. You're doing it for your links, but not your folders, so those IDs are going to keep changing out from underneath you.

## JavaScript Style

**13 points**: Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

* You shouldn't need either of [these](https://github.com/JustynaField/jet-fuel/blob/master/server.js#L22-L23) as you have a database setup now.

* Setting up your newLink like [this](https://github.com/JustynaField/jet-fuel/blob/master/server.js#L86-L90) is dangerous because if any of those `request.body` values are missing, you're immediately going to have something set as undefined. Your conditional check for required parameters after the fact isn't doing much because you're already assuming all of those values exist. I would refactor this to just say `let newLink = request.body` and then add a shortUrl property to that object.

* There is a status code you can use for [redirects](https://github.com/JustynaField/jet-fuel/blob/master/server.js#L122)...

* You're [deferring](https://github.com/JustynaField/jet-fuel/blob/master/public/script.js#L2) `fetchFolders` until the document is ready --- fetch requests are not dependent on the DOM being ready. You should kick this off immediately and only include functions that depend on the DOM in document.ready.

* Instead of [re-fetching all the folders](https://github.com/JustynaField/jet-fuel/blob/master/public/script.js#L11) after a POST request, I would simply return the single, new folder from the server and append that one to the DOM. There's no need to re-fetch the entire collection if all you're going to do is append a new item to the dom.

* Just an FYI/nitpick, 'print' is a weird name for functions like [this](https://github.com/JustynaField/jet-fuel/blob/master/public/script.js#L32). When we hear print we generally thing physical ink and paper. For the web, a better term would be 'appendAllFolders'

* [Noooo](https://github.com/JustynaField/jet-fuel/blob/master/public/script.js#L167)

## Workflow

**13 points**: The developer makes a series of small, atomic commits that document the evolution of their application. There are some formatting issues in the code base, some commits would've been better on branches.

* Would like to see more use of feature branches rather than committing straight to master
* Another file you want to make sure to .gitignore is this [DS_Store](https://github.com/JustynaField/jet-fuel/blob/master/.DS_Store) file
* Nice, consistently formatted commit messages though I would recommend starting them all with a capital letter.  [This](https://chris.beams.io/posts/git-commit/) is a good set of rules to follow for formatting your commit messages.
* [Some](https://github.com/JustynaField/jet-fuel/commit/ad4cf691ba18813148882b16de5c6edf04e5d860) commits would have been better on a branch rather than committed to master, especially when they contain commented-out code or are a work in progress.


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: 125 / 160
