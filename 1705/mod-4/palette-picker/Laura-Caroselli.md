# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/lcaroselli/palette-picker)

#### Link to the Deployed Application
[heroku](https://paletter-picker-1000.herokuapp.com/)
**Note: Heroku isn't updating with my most recent changes...

#### Link to your annotated server file
[annotated server file](https://github.com/lcaroselli/palette-picker/tree/lc-code-comments-2)

## Completion

#### Were you able to complete the base functionality?
Yes

#### Which extensions, if any, did you complete?
N/A

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/lcaroselli/palette-picker/commit/7b137592581e610b7c5ce664b86644e5696491f2)

* Why were you proud of this piece of code?
I was finally able to get the page to update the DOM with projects and palettes without needed to refresh - it took a while to think this logic through.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code]()
Nothing specific, but I am aware that there is a bit of code duplication going on and I could have refactored a lot of the functionality for displaying projects and palettes to the page.


#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
[test suite]()
My test suite is running sporadically and I think it has something to do with the server it's trying to run on, but I can't figure out how to fix it. All tests passed before trying to run my project with nodemon again...

#### Please feel free to ask any other questions or make any other statements below!

This project was fun, but there was a lot to learn and to accomplish crammed into 4 days. Maybe spread this project out over a longer period of time so students can feel confident in their learning and complete the project. I feel like I sacrificed parts of my learning for the sake of trying to get more of the project done, and I'm not comfortable with that.

Anything else you wanna say!

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**40 points**: (50 possible points)

- Cannot save a palette to a project in production (saw gif of everything working locally), but production is a part of this project - deducting a bit because of that
- Missing minor feature where clicking on a saved palette will update the top colors to the colors of the saved palette

## User Interface

**15 points**: (20 possible points)

- The form looks good, but there needs to be some room on the left of the placeholder text within the input fields
- Need some space between project groups
- I would keep the width of the project containers the same even when they do not have any palettes in them - when they shrink, they look a little awkward all with different sizes

## Data Persistence with SQL Database

**20 points**: (20 possible points)

- Schema looks good with one-to-many relationship using primary/foreign key

## Testing

**10 points**: (20 possible points)

- Good job with the before and beforeEach blocks
- [This 404 test](https://github.com/lcaroselli/palette-picker/blob/master/test/routes.spec.js#L64) and [this test](https://github.com/lcaroselli/palette-picker/blob/master/test/routes.spec.js#L99) are actually testing the same mechanism in Express to handle unknown routes, so you only need to test this once
- Good [sad path test here](https://github.com/lcaroselli/palette-picker/blob/master/test/routes.spec.js#L124), but should respond with a 404 because the resource cannot be found
- I don't see any happy or sad path tests for POST routes

## Commented Server File

**5 points**: (10 possible points)

- Some lines and groups of code missing comments
- Instead of groups of comments, we're looking for comments on each line so we know what sentence goes with a certain line of code
- [This line](https://github.com/lcaroselli/palette-picker/blob/lc-code-comments-2/server.js#L26) is pretty vague, there are a few pronouns that I don't know what you're referring to

## JavaScript Style

**12 points**: (20 possible points)

- [This](https://github.com/lcaroselli/palette-picker/blob/master/server.js#L20) is a strange thing to have since you are sending static assets and don't want to send information in the body
- Good job using a `.catch()` for all of your server-side promises
- For this case of [no resources in the table](https://github.com/lcaroselli/palette-picker/blob/master/server.js#L28), it is not actually a 404 because the endpoint is valid, there are just no things in the table - so send a 200 response with an empty array, that's ok - same with palettes
- Good response [here](https://github.com/lcaroselli/palette-picker/blob/master/server.js#L75) - just change the status code to 404
- Using the same variable [here](https://github.com/lcaroselli/palette-picker/blob/master/public/js/scripts.js#L24-L26) and other spots is pretty confusing since they represent the response in different ways
- Instead of using the `id` [attribute](- Instead of using the `id` [attribute](https://github.com/mschae16/palette-picker/blob/master/public/js/scripts.js#L36), use `data` attributes to store data about a DOM node, same with palettes), use `data` attributes to store data about a DOM node, same with palettes
- Why return the [response twice](https://github.com/lcaroselli/palette-picker/blob/master/public/js/scripts.js#L198-L199)? You can just use one line to convert the response to JSON

## Workflow

**20 points**: (20 possible points)

- Good small commits using imperative subject lines with a lot of branches - keep it up

### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: 122 / 160
