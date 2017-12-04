# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/lolakoala/palette-picker)

#### Link to the Deployed Application
[heroku](https://lolas-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/lolakoala/palette-picker/tree/comments)

## Completion

#### Were you able to complete the base functionality?

Yes! 

If not, explain what is missing and why.

#### Which extensions, if any, did you complete?

I did not complete any extensions.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/lolakoala/palette-picker/blob/master/public/scripts/scripts.js#L21-L42)

* Why were you proud of this piece of code?

Each project gets it's own palettes on page load, and then puts the colors of each palette into an array. I map through the array to create an html tag for each color, and then I append it to the page. I thought this was a sleek solution to appending the color palettes.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/lolakoala/palette-picker/blob/master/public/scripts/scripts.js#L66-L94)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

In this code, I'm toggling the lock img attributes on click of both the color div and the image. I expected it to work on the img (which is inside the div) without having to code it on click due to event bubbling... When it did not behave as expected, I basically had to duplicated some code and change the selector. I was nervous about refactoring this into one function because the code is just different enough that I'm not sure what I would pass in to handle that.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

12 passing (513ms)
  1 failing

  1) Uncaught error outside test suite:
     Uncaught Error: listen EADDRINUSE :::3000


#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

[art bag image](https://dribbble.com/shots/313499-Artist-Bag-Icon)

I was inspired by this image to make my app art-themed. I envision my app being used by art students/teachers.

[circles image](https://dribbble.com/shots/1710723-Brawker-The-new-color-palette)

I use a lot of circles and rounded corners in my designs, but these circles really helped me envision how I wanted the random color palette to look. I found this before the art supplies bag, so when I found that I ended up placing the circles on the paint palette image.

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

The design of this project was a lot of fun! I am enjoying learning about the backend. 

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
