# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/meloncatty/palette-picker)

#### Link to the Deployed Application
[heroku](https://kh-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/meloncatty/palette-picker/tree/iteration-002)  
This branch became 'unmergable' after I accidentally reinstalled knex.
Tests are not working, though they are annotated anyway.

## Completion

#### Were you able to complete the base functionality?

No. I did not have enough front-end functionality completed by the time I started working on implementing endpoints. Not able to parse error coming back from DELETE, so that is not implemented.

#### Which extensions, if any, did you complete?

None.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/meloncatty/palette-picker/blob/c281405c3b4f70663e5f3b5acff53c17cc430d25/public/src/index.js#L167-L179)

* Why were you proud of this piece of code?  
This was the first function in my code that began to grow, and once it was finished I knew it was time to break things out into smaller functions. It was difficult to figure out how to append elements correctly after breaking it out, but I am happy with the end result.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/meloncatty/palette-picker/blob/c281405c3b4f70663e5f3b5acff53c17cc430d25/public/src/index.js#L200-L224)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
The functionality inside of the `try...catch` mirrors the code in my 'happy code'. Instead of creating the element variables inside the 'happy code' it might have been best to pass those variable in as parameters in order to make it more dynamic, thus making the 'sad code' more happy.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

[Material-UI](https://material.io/design/components/text-fields.html)
I like their simple form fields and buttons.

[Material-UI](https://material-ui.com/demos/paper/)
I also like their papers!

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

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
