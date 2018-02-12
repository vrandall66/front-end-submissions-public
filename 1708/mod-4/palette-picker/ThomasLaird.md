# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/t-laird/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-thomas-laird.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/t-laird/palette-picker/blob/server-comments/server.js)

## Completion

#### Were you able to complete the base functionality?

Yes.

#### Which extensions, if any, did you complete?

None.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/t-laird/palette-picker/blob/56c793a0c893a1df14de1747537bb1a85ca108d1/public/js/scripts.js#L53-L59)

* Why were you proud of this piece of code?

I thought this was an elegant solution for grouping the set of DOM elements that were frequently referenced and changed throughout palette picker. This data structure allowed me to easily maintain the rest of the core interactions of the app.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/t-laird/palette-picker/blob/56c793a0c893a1df14de1747537bb1a85ca108d1/public/js/scripts.js#L382-L392)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

A lot of the areas of inefficiency here are when I had to use non-straightforward methods to strip project or palette ids from the DOM. This block of code uses a regex and match to strip the project id off the end of the project's class name. A better solution would probably be storing that information in a different attribute that could be accessed more directly.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

![test suite](https://raw.githubusercontent.com/t-laird/palette-picker/master/palette-picker-tests.png?raw=true)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

[dribble](https://dribbble.com/shots/3581514-Suspension-light-balls)

I have previously used coolors to come up with color palettes for other projects, but have often found that the palette alone doesn't give a great indication of how the colors might mix or blend together. I used this dribbble creation as inspiration to make some visualization of the palette colors using HTML canvas.

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

