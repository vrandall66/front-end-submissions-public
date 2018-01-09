# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/AdamMescher/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-adam-mescher.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/AdamMescher/palette-picker/blob/am-commented-server-file/server.js)

## Completion

#### Were you able to complete the base functionality?

I was able to complete the base functionality. 

#### Which extensions, if any, did you complete?

I did not complete any extensions for this project that were listed in the project spec. I did implement the ability to delete projects. 

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code 1](https://github.com/AdamMescher/palette-picker/blob/master/server.js#L67-L87)

* It was interesting learning about the .first() method which allows a query to stop at the first found item rather than iterate through the entire column.

[happy code 2](https://github.com/AdamMescher/palette-picker/blob/master/public/js/scripts.js#L283-L291)

* It was fun figuring out the animation for continued rotation of the button and color wheel.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/AdamMescher/palette-picker/blob/master/public/js/scripts.js#L49-L64)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

- This is not a pure function as it does multiple things, and since the promise resolves it still posts the project to the page. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://imgur.com/a/mcdoI)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

[Color Aperture inspiration from Dribble](https://dribbble.com/shots/891640-Colour-Palettes)
[Palette Card inspiration from Dribble](https://dribbble.com/shots/3340684-Color-Palette-Component)

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**45 points**: (50 possible points)

* Missing the functionality where clicking on a saved palette changes the main palette picker
* Everything else looks good

## User Interface

**15 points**: (20 possible points)

* The palette wheel is pretty cool! I'm not sure what purpose it serves other than visual - I glad the palette on the right changes immediately because users get frustrated when animations take too long and slow them down
* The new project form was a little hard to use at first, wasn't sure which part was a form or just text
* Why is the hover-expansion of the top-right palette colors needed?

## Testing

**x points**: (20 possible points)

* Need to complete API testing

## Commented Server File

**6 points**: (10 possible points)

* [This](https://github.com/AdamMescher/palette-picker/blob/am-commented-server-file/server.js#L11) doesn't "return" middleware, but it does set up middleware - need some more context around why we need to use body parser (to parse what JSON and why do we need the package?)
* Want some more details around the configuration passed in [here](https://github.com/AdamMescher/palette-picker/blob/am-commented-server-file/server.js#L27)
* ["do the thing"](https://github.com/AdamMescher/palette-picker/blob/am-commented-server-file/server.js#L44)?
* Overall, good comments, but some are very broad/vague

## JavaScript Style

**x points**: (30 possible points)

* You have [this line](https://github.com/AdamMescher/palette-picker/blob/master/server.js#L22) in your server file twice
* [This](https://github.com/AdamMescher/palette-picker/blob/master/server.js#L81-L85) is a good portion of code where you could refactor into its own function or middleware since you're doing the same thing in another POST request route handler - the only difference is the params that are expected
* Good job sending a 404 [here](https://github.com/AdamMescher/palette-picker/blob/master/server.js#L148) - many people in your class were sending a 422 instead, which is not correct
* Be sure you send an appropriate [status code here](https://github.com/AdamMescher/palette-picker/blob/master/server.js#L139) with your error response
* Good job using `catch()` with all of your client-side fetch calls
* One thing to note with using `fetch` is that it will not error on 404 - in order to hit the `.catch` on a 404, you can check for `response.ok` [demonstrated in the MDN docs here](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch#Checking_that_the_fetch_was_successful)
* Careful not to leave [commented-out code](https://github.com/AdamMescher/palette-picker/blob/master/public/js/scripts.js#L97) in your source
* This whole section of [dense code](https://github.com/AdamMescher/palette-picker/blob/master/public/js/scripts.js#L95-L125) is really hard to parse through, don't be afraid to add some space
* I would probably move the code for the color wheel to another file - there is a good amount of functionality around it that isn't related to the core of the page
* Consider moving [this](https://github.com/AdamMescher/palette-picker/blob/master/public/js/scripts.js#L214-L236) to an HTML template

## Workflow

**15 points**: (20 possible points)

* Good to see that you were Waffle for this project - people viewing repos like to see that you still have pending issue too, which lets them know you are still working on the project of if something is not complete
* Need smaller, more atomic commits (would expect nearly 100 commits for this project)
* Good job adding `.gitignore` to project early on


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150

