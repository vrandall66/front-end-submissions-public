# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/Cache123/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-sam-singer.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/Cache123/palette-picker/blob/master/server.js)

## Completion

#### Were you able to complete the base functionality?

Most of the base functionality is there, with the exception of project names being unique. Will need to update that on the server side and have some sort of error message display if a user attempts to add an existing project.

#### Which extensions, if any, did you complete?

None.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/Cache123/palette-picker/blob/master/public/js/scripts.js#L20-L23)

* I spoke to other students about how they toggled their classes and my solution seemed much easier and straightforward!

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/Cache123/palette-picker/blob/master/public/js/scripts.js#L118-L136)

* Sad code since there's no validation for inputing project names.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
[test suite](https://github.com/Cache123/palette-picker/blob/master/test/routes.spec.js)

💻  palette-picker 💻  mocha


running on 3000.
  Client Routes
    ✓ should display the homepage correctly
    ✓ should return a 404 if the route does not exist

  API Routes
    GET /api/v1/projects
      ✓ should get projects from database
      ✓ should return 404 for a bad URL
    GET /api/v1/palettes
      ✓ should get palettes from database
      ✓ should return status 500 if project does not exist


  6 passing (130ms)


#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

[dribble inspiration](https://www.wix.com/website-template/view/html/1945/?siteId=70207374-ba42-48b4-97d0-a270ec1de7b0&metaSiteId=aad5ee72-e7e2-480f-8e36-2693a67813e6&originUrl=https%3A%2F%2Fwww.wix.com%2Fwebsite%2Ftemplates%2Fhtml%2Flanding-pages)

I really appreciated how simple the front landing page was, so tried to incorporate that into my design and pushing everything out that was extra out of sight and toward the bottom. Such as creating and saving palettes and projects.

Testing is difficult and I still don't fully understand why it's breaking when I POST, but have a general idea of why.

-----


# Instructor Feedback (Instructor Name)

## Specification Adherence

**x points**: (50 possible points)

## User Interface

**x points**: (20 possible points)

## Testing

**x points**: (20 possible points)

## Commented Server File

**x points**: (10 possible points)

## JavaScript Style

**x points**: (30 possible points)

## Workflow

**x points**: (20 possible points)


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
