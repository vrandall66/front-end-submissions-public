# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/patrickjneel/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-pn.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/patrickjneel/palette-picker)

## Completion

#### Were you able to complete the base functionality?
No.

If not, explain what is missing and why.
I got hung up on getting the plalettes by the name and didn't get to the delete functionality.

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code]()

* Why were you proud of this piece of code?
I think the basic design was ok

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/patrickjneel/palette-picker/blob/4e02e7b3a60d6cdd0c43f386ae6b60ccf8ede8df/public/js/scripts.js#L170)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
I don't feel confident that it is posting corerectly to the back end
#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it
I looked through dribble for border-radius that looked alright.
#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**30 points**: (50 possible points)

* Palettes aren't persisting in the Projects section of the page on refresh
* Bug: Hex values string keeps getting longer every time you save a new palette
* Missing delete functionality (like you noted in your submission)

## User Interface

**13 points**: (20 possible points)

* The initial state of the app around palette generation is effective and easy to use
* The flow for creating a project is a little hard to follow when you first use the page
* Display of the hex values for a saved palette is hard to read (the text is scrunched together), and there is no color representation

## Testing

**10 points**: (20 possible points)

* Just testing for an object [here](https://github.com/patrickjneel/palette-picker/blob/master/test/routes.spec.js#L45-L46) is not very robust - should test for structure within the object (like properties); this applies to other tests in your tests suite as well
* [The error should be thrown](https://github.com/patrickjneel/palette-picker/blob/master/test/routes.spec.js#L45-L46) instead of returned so you get the proper error response when you run the test suite - otherwise, it will appear as if the test is passing when you run the test suite when it is actually failing
* Good job responding with 201 status code for [POST request](https://github.com/patrickjneel/palette-picker/blob/master/test/routes.spec.js#L73)
* Testing for property [here](https://github.com/patrickjneel/palette-picker/blob/master/test/routes.spec.js#L75) is good - would want to test for actual value of the project name in the response
* [This test](https://github.com/patrickjneel/palette-picker/blob/master/test/routes.spec.js#L83-L97) is not testing the projects endpoint, and the expected response in the test does not have the correct status code (201 means successful POST...)
* Missing sad paths for DELETE and POST requests

## Commented Server File

**7 points**: (10 possible points)

* Good job being thorough commenting on most lines - in general, your comments are a bit vague when you're talking about the technical details

## JavaScript Style

**17 points**: (30 possible points)

* I would expect [this endpoint](https://github.com/patrickjneel/palette-picker/blob/master/test/routes.spec.js#L45-L46) to return an array - for [this line](https://github.com/patrickjneel/palette-picker/blob/after-friday/server.js#L31), would just expect to send back array of projects instead of wrapping it in an object, [same issue here with palettes](https://github.com/patrickjneel/palette-picker/blob/after-friday/server.js#L42)
* [This line](https://github.com/patrickjneel/palette-picker/blob/after-friday/server.js#L19) for body-parser is not needed because you are not getting URL-encoded data, only JSON data in the body of a request (you only need [this line](https://github.com/patrickjneel/palette-picker/blob/after-friday/server.js#L18) for JSON coming in the body of a request)
* Generally, [table names are plural](https://github.com/patrickjneel/palette-picker/blob/after-friday/db/migrations/20180124144324_third_update.js#L10)
* If there [aren't any palettes in the database](https://github.com/patrickjneel/palette-picker/blob/after-friday/server.js#L44-L47), then just return the empty array (it's not an error, there is just nothing in the database table - send a 200 response with the empty array)
* Good error response [here](https://github.com/patrickjneel/palette-picker/blob/after-friday/server.js#L56-L62)
* For [this request](https://github.com/patrickjneel/palette-picker/blob/after-friday/server.js#L76), the data you need about the project is the ID, which is in the URL - I see you also have the `projectName` in the request body, which is redundant
* [This endpoint](https://github.com/patrickjneel/palette-picker/blob/after-friday/server.js#L92) should just be `api/v1/palettes/:id` because you only need the `:id` of the palette to know which palette to delete

## Workflow

**18 points**: (20 possible points)

* Good number of commits
* Good job adding gitignore, especially for node_modules
* Commits should use present tense (you were mixing present and past tense in some of your commit titles)

### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 95 / 150
