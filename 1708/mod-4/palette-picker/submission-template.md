# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/rmorgan323/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-rmorgan323.herokuapp.com/)

#### Link to your annotated server file
[annotated server file]()

## Completion

#### Were you able to complete the base functionality?

Yes!

#### Which extensions, if any, did you complete?

I added:
Delete projects
See/modify existing palettes by clicking on the colors.  That will push them back up to the main section.  Also, the user can edit palette names.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/rmorgan323/palette-picker/blob/0dffe5c1c95ecaa6ab0eaf86538061fb7cc882ed/public/js/scripts.js#L354)
[happy code](https://github.com/rmorgan323/palette-picker/blob/0dffe5c1c95ecaa6ab0eaf86538061fb7cc882ed/public/js/scripts.js#L380)
These are a couple of helper functions that I made in order to display hex value text and lock images either white or black, depnding on the background color.  I think it really adds to the UI, making it easy to see.

[happy code](https://github.com/rmorgan323/palette-picker/blob/0dffe5c1c95ecaa6ab0eaf86538061fb7cc882ed/public/js/scripts.js#L97)
This is a helper function used by updatePalette to create the correct body for the fetch.  It enables the updatePalette function to be used to update any value, not just the name.  While I haven't created the ability to edit colors in a palette yet, this is the function that would make that possible.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/rmorgan323/palette-picker/blob/0dffe5c1c95ecaa6ab0eaf86538061fb7cc882ed/public/js/scripts.js#L245)
I ended up writing two different appends for palettes since one version needs an input box and the other an h5.  I didn't have the time to go back and figure out a cleaner way to write this.  It'd be better with just one append.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
[test suite]()
I only have 3 working tests right now but will have more by tomorrow.

#### Link to Design Inspiration
I liked the large color blocks on Coolors and ended up thinking through the design with that.  I initally made everything in greyscale and allowed the color blocks to be the only colors on the page.  Then I showed the design to Louisa who liked the grey and thought I should just leave it!  So I did.  I think the fact that the site is grey and the color palettes are the only colors on the page makes the UI very clean and easy-to-understand.

#### Please feel free to ask any other questions or make any other statements below!

Some of the details are not as done as I want them to be.  I'll work on this some more tonight and tomorrow.  Thank you for your understanding.

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

