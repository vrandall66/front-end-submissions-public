# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/EvanSays/jetfuel)

#### Link to the Deployed Application
[heroku](https://jetfuelturbo.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/EvanSays/jetfuel/blob/em-comments/server.js)

## Completion

#### Were you able to complete the base functionality?

No, I am missing the functionality of having each folder expand when clicked upon. Time was the limiting factor, due to a slow work pace and missing a night to code to focus on my Demo Night performance. All the other functionality is there. I'm happy with the result, but would of loved to implement that final piece.
 
#### Which extensions, if any, did you complete?

None.

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/EvanSays/jetfuel/blob/master/public/main.js)

* Why were you proud of this piece of code?

Line 27: I like that added the check to see if all the input fields were not blank when a user submits their url. On Line 36, I found a way to grab the selection on a drop down. This was extremely useful for me to to compare and filter links later on.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/EvanSays/jetfuel/blob/master/public/styles.css)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

The CSS and HTML are a cluster mess imo. This was partly due to rushing through the project. If I had to refactor something on this project, I would jump to clean these up a bit.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
 ▲ assignments/4-mod/jetfuel mocha                                                                                                          master :: 7s :: ⬢


jetfuel is running on 3000.
  Client Routes
    ✓ should return the homepage with text
    ✓ should return a 404 for a route that does not exist

  API Routes
Re-seed complete!
    ✓ GET /api/v1/folders
    GET /api/v1/links
Re-seed complete!
      ✓ should get all the links
    POST /api/v1/folders
Re-seed complete!
      ✓ should create a new folder
Re-seed complete!
      ✓ should not create a folder with missing data
Re-seed complete!
      ✓ should not create a folder with the same name
    POST /api/v1/links
Re-seed complete!
      ✓ should create a new link
      - should not create a link with missing folder_id
    GET /api/v1/folders/:id/
Re-seed complete!
      ✓ should get all the links in a specified folder
Re-seed complete!
      ✓ should not get a link if the folder number does not exist
    GET /api/v1/folders/${id}/links
Re-seed complete!
      ✓ should get a link by id
Re-seed complete!
      ✓ should not get a link if the id number does not exist


  12 passing (643ms)
  1 pending
```

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

Overall, a fun project to practice using jQuery again. I also enjoyed going full circle with Heroku and CircleCI. 

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
