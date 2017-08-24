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

**20 points**: There are two features missing from the base expectations that make the application feel incomplete or hard to use.

## User Interface

**x points**: Lorem ipsum dolor set amet

## Data Persistence with SQL Database

**18 points**: The application persists data in a SQL database but with correct relationships between folders and URLs, slight error with column fields re: uniqueness

* The [shortUrl](https://github.com/JustynaField/jet-fuel/blob/master/db/migrations/20170816132247_initial.js#L14) must be a unique value. If you generate two of the same short URLs, that point to different long URLs, one of them will be overridden. 
 
## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**13 points**: The developer makes a series of small, atomic commits that document the evolution of their application. There are some formatting issues in the code base, some commits would've been better on branches.

* Would like to see more use of feature branches rather than committing straight to master
* Another file you want to make sure to .gitignore is this [DS_Store](https://github.com/JustynaField/jet-fuel/blob/master/.DS_Store) file
* Nice, consistently formatted commit messages though I would recommend starting them all with a capital letter.  [This](https://chris.beams.io/posts/git-commit/) is a good set of rules to follow for formatting your commit messages.
* [Some](https://github.com/JustynaField/jet-fuel/commit/ad4cf691ba18813148882b16de5c6edf04e5d860) commits would have been better on a branch rather than committed to master, especially when they contain commented-out code or are a work in progress.


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: x / 150
