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

I feel that I have all of the basic functionality working, except for these two pieces:

- Visit a folder and sort the folder’s URLs by how recently they were added (both descending and ascending order)
- Enter a URL to be shortened only if it is a valid URL (impose some kind of URL validation)

I ran out of time, also I found it a little complex and time-consuming.

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/JustynaField/jet-fuel/blob/master/server.js),
[happy code](https://github.com/JustynaField/jet-fuel/blob/master/db/test/seeds/folders.js)

* Why were you proud of this piece of code?

#### Link to a specific block of your code on Github that you feel not great about
[sad code]()

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
  Client Routes
    ✓ Should return homepage (47ms)
    ✓ should return a 404 for a route that does not exist

  API Routes
    GET /api/v1/folders
travel
      ✓ should return all of the folders
    GET /api/v1/folders/:id
      - should return folder by id
travel
      ✓ should return an error if a requested folder does not exist
    POST /api/v1/folders
travel
      ✓ should create a new folder (40ms)
travel
      ✓ should not create a record with missing data
    GET /api/v1/links
travel
      ✓ should return all of the links
    POST /api/v1/links
travel
      ✓ should post a new link
double callback!
      - should not create link if required data is missing
    GET /api/v1/folders/:id/links
travel
      ✓ should return links belonging to a specific folder
      - should not return links for folrder that does not exist


  9 passing (828ms)
  3 pending
```

#### Test suite:
[test suite](https://github.com/JustynaField/jet-fuel/tree/master)



#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Instructor Name)

## Specification Adherence

**x points**: Lorem ipsum dolor set amet

## User Interface

**x points**: Lorem ipsum dolor set amet

## Data Persistence with SQL Database

**x points**: Lorem ipsum dolor set amet

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**x points**: Lorem ipsum dolor set amet


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: x / 150
