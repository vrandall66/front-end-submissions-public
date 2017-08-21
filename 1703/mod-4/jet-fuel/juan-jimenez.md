# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/jdiejim/Jet-Fuel)

#### Link to the Deployed Application
[heroku](https://jdj-jet-fuel.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/jdiejim/Jet-Fuel/blob/jdj-server-comments/server.js)

[annotated router file](https://github.com/jdiejim/Jet-Fuel/blob/jdj-server-comments/router.js)

[annotated folder controller file](https://github.com/jdiejim/Jet-Fuel/blob/jdj-server-comments/controllers/foldersController.js)

[annotated folder model file](https://github.com/jdiejim/Jet-Fuel/blob/jdj-server-comments/models/Folder.js)

[annotated path controller file](https://github.com/jdiejim/Jet-Fuel/blob/jdj-server-comments/controllers/pathsController.js)

[annotated path model file](https://github.com/jdiejim/Jet-Fuel/blob/jdj-server-comments/models/Path.js)


## Completion

#### Were you able to complete the base functionality?

Yes :)

#### Which extensions, if any, did you complete?

No extensions :(

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/jdiejim/Jet-Fuel/blob/master/src/views/Collections.js#L1-L97)

* Why were you proud of this piece of code?

I tried to mimic the structure and workflow of React, and separated the views in different files. I was able to handle the views' functionality more easily, and putting it all together was easier.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/jdiejim/Jet-Fuel/blob/master/test/routes.spec.js#L17-L24)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

This works but it does not follow the template we saw in class. It took me a while to make it work. I was confused with the before, and after hooks, and decided to discard them, and instead use before each to rollback 2 migrations, run latest, and reseed for each test.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```

API ROUTES
  GET /api/v1/folders
Seeding complete!
Seeding complete!
Seeding complete!
    ✓ should return all folders
  POST /api/v1/folders
Seeding complete!
Seeding complete!
Seeding complete!
    ✓ should not create folder with missing data
Seeding complete!
Seeding complete!
Seeding complete!
    ✓ should create a new folder (38ms)
  DELETE /api/v1/folders
Seeding complete!
Seeding complete!
Seeding complete!
    ✓ should not delete folder if missing data
Seeding complete!
Seeding complete!
Seeding complete!
    ✓ should delete a folder
  GET /folders/:id/paths
Seeding complete!
Seeding complete!
Seeding complete!
    ✓ should return all paths from specific folder
  POST /folders/:id/paths
Seeding complete!
Seeding complete!
Seeding complete!
    ✓ should create new path for a specific folder
Seeding complete!
Seeding complete!
Seeding complete!
    ✓ should not create new path with missing data

8 passing (944ms)

```

#### Please feel free to ask any other questions or make any other statements below!

I tried for fun using an MVC architecture, and created 2 models that handle the interaction with the database. 2 controllers that handled the requests and responses, and two views made with jQuery. It has a lot of files, but I found it easier to maintain and understand. I wanted to ask you if there are better ways of structuring node servers?

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
