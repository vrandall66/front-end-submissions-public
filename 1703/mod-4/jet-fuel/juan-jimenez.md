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

# Instructor Feedback (Brittany)

## Specification Adherence

**x points**: Lorem ipsum dolor set amet

* URL validation is off or unrecognizable - I can't type in a URL that is www.nhl.com and have the short URL bring me to the NHL website. (It tries to bring me to https://jdj-jet-fuel.herokuapp.com/www.nhl.com instead)

## User Interface

**12 points**: The application shows a lot of effort in the interface, but there are a few things that make the interactions a bit confusing. The evaluator has some difficulty using the application when reviewing the features in the user stories.

* I like how you broke out the flow of the user interaction to let the user focus solely on creating a URL first, then assigning it to a folder, but the timing of when the folder selection shows up is a little bizarre. Instead of having it show up as soon as I key into the URL field, I would wait until the user has a valid URL in the input. 
* Top left logos usually link you back to the default/home page, I'd make this a link to the shorten page
* I'd expect to be able to click on a folder and have it show me the collections page and the URLs - it's also weird that the 'Save' buttons still exist on the list of folders even after I've saved my URL and the input boxes have been cleared out.
* The 'URL not valid' message sticks around long after I've entered a new valid url. 
* The overflow: scroll on all your containers is a little offputting, when there is no scroll it looks like you have very large white borders on the right and bottom of all your elements.
* It's difficult to tell that the sorting arrows are going to sort the URLs by date. I'd add a label to those or make them line up more closely with the dates in the URL list.
* There's some bizarre bug where I can click on the top border of the URL list and the urls will completely disappear. Clicking one of the sorting arrows makes them return.


## Data Persistence with SQL Database

**18 points**: The application persists data in a SQL database but with correct relationships between folders and URLs, slight error with column fields re: uniqueness

* The [shortUrl](https://github.com/jdiejim/Jet-Fuel/blob/master/db/migrations/20170815171324_paths.js#L10) must be a unique value. If you generate two of the same short URLs, that point to different long URLs, one of them will be overridden. 
 
**x points**: Lorem ipsum dolor set amet

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**14 points**: The developer makes a series of small, atomic commits that document the evolution of their application. There are some formatting issues in the code base.

* ~40 commits likely isn't enough for the scope of this project. Commits like [this](https://github.com/jdiejim/Jet-Fuel/commit/1c44d676ca9b1a053b29c2d1191314af69b67efd) are doing way too much. Pull requesting a diff this large in a single commit would make it more difficult for teammates to do a code review on it.
* Good use of branches, though I'm not sure I would prefix their names with your initials. (You may have been told to do this by previous mentors/instructors). Just as an FYI I've never seen that convention in the real world. Multiple people can actually work on branches so it might not make sense all the time. I would stick to naming them in regards to what functionality they'll be adding.
* Nice, consistently formatted commit messages though I would recommend starting them all with a capital letter. [This](https://chris.beams.io/posts/git-commit/) is a good set of rules to follow for formatting your commit messages.

### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: x / 150
