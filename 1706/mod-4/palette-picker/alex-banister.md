
# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/alexbanister/palette-picker)

#### Link to the Deployed Application
[heroku](https://ahb-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/alexbanister/palette-picker/blob/comments/server.js)

## Completion

#### Were you able to complete the base functionality?

* Functionality complete. Couldn't complete tests. I have happy and sad paths for GET, POST, and DELETE projects but couldn't get palette endpoint tests to work. I think I was having a problem with the primary keys of projects and palettes auto incrementing and seed not resetting it. Tried adding .truncate() to the .del() in test seed file but psql won't let me do that. I tried .raw('ALTER SEQUENCE id RESET WITH 1') or something along those lines but also didn't work.

#### Which extensions, if any, did you complete?

* None, but I did add a random name suggestion to palettes and projects sort of the way repl does.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/alexbanister/palette-picker/blob/df99d3388b24b379f1208f903adec0bb52764c17/src/index.js#L99-L116)

* Building DOM elements seems to always get super messy. This function is a bit longer than I'd like and there is a bit more complexity than I like but I'm happy with it's cleanliness and readability.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/alexbanister/palette-picker/blob/df99d3388b24b379f1208f903adec0bb52764c17/src/index.js#L147-L165)

* This function kept growing as I developed and got messy, hard to read and does too much.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
<img width="753" alt="screen shot 2017-12-01 at 11 59 15 am" src="https://user-images.githubusercontent.com/17756439/33498598-316c1968-d68f-11e7-95f4-12997a4f270a.png">

#### Link to Design Inspiration

[Inspiration](https://dribbble.com/shots/2761157-Brisk-Mate-Branding-Guidelines-Color-Pallete)

* I liked the "droplet" color dots and thought they would be a nice way to show colors and how they interact with the palette. the rest of the design was build around that.

#### Please feel free to ask any other questions or make any other statements below!

* Test seems better than DOM testing but still a bit squirrelly and I don't really understand how to debug tests and how to make them work consistently. 

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**x points**: (50 possible points)

## User Interface

**x points**: (20 possible points)

## Data Persistence with SQL Database

**x points**: (20 possible points)

## Testing

**x points**: (20 possible points)

## Commented Server File

**x points**: (10 possible points)

## JavaScript Style

**x points**: (20 possible points)

## Workflow

**x points**: (20 possible points)


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: x / 160
