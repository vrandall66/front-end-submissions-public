# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/robbiegreiner/palette-picker)

#### Link to the Deployed Application
[heroku](https://robbie-greiner-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/robbiegreiner/palette-picker/blob/server-comments/server.js)

## Completion

#### Were you able to complete the base functionality?

Yes, I completed all base functionality.

#### Which extensions, if any, did you complete?

I completed the extension to be able to edit the hex of a color.

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://gist.github.com/robbiegreiner/d59c563fc517df2921935e9c6610f830)

* Q: Why were you proud of this piece of code?
* A: I like this because I think that using a dynamic ID is way easier than I thought it would be. I feel like this is as
clean as it could possibly be.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://gist.github.com/robbiegreiner/d59c563fc517df2921935e9c6610f830)

* Q: Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
* A: I feel instead of making all 5 of these divs individually, I could iterate through and create each DIV. But I struggled to run a for loop inside of the html.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]![screen shot 2017-12-01 at 11 04 56 am](https://user-images.githubusercontent.com/28495779/33496463-8cff5464-d687-11e7-8d45-be67ee4c9ca2.png)

#### Link to Design Inspiration

* Q: Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it
* A: I used http://www.yeticycles.com/ I really like their primary colors, their buttons and their header.  I find the color and cleanliness of their site appealing.

#### Please feel free to ask any other questions or make any other statements below!

The lessons in class so far have been extremely well written and they are easy to follow.  They made getting through this project a lot less stressful along with helping me learn.

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**55 points**: (50 possible points) No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use. Data persists on refresh using a knex/postgreSQL database.

* Nice job getting an extension in - but the UI for it is a little funky. Would like some visual indicator that you can edit that hex code value. (Maybe a little 'edit'/'pencil' icon?) and would be nice to have the HEX value update, and pop you out of the text input when you hit the ENTER key. You can add key-code specific events with jQuery to blur yourself out of an input like that. Additionally, if I make the HEX value white, I lose the ability to see the HEX value text. Would be good to change that text to a dark color when white is the chosen color.

## User Interface

**18 points**: (20 possible points) User interface is intuitive and the instructor can easily use it on their own without guidance. Styling is consistent and call-to-action elements are obvious. The application provides the user with relevant feedback based on interactions.

* Nice, simple UI, easy to use. Would be nice to display a 'No projects/No Palettes' message for any projects that don't contain palettes.

## Testing

**15 points**: (20 possible points) Project has a running test suite that tests every server-side endpoint, but only has a couple sad path cases.

* No [.catch](https://github.com/robbiegreiner/palette-picker/blob/master/test/routes.spec.js#L31) here or [here](https://github.com/robbiegreiner/palette-picker/blob/master/test/routes.spec.js#L75) :(

* There's actually no guarantee that your data will come back in a specific order unless you are explicitly sorting it. So assertions like [these](https://github.com/robbiegreiner/palette-picker/blob/master/test/routes.spec.js#L99-L117), where you're dependent on certain values existing at a particular index of an array often have intermittent failures. It doesn't look like you're sorting your data any where in your server file so I'd be surprised if this was consistently working for you.

* Your assertions in [this](https://github.com/robbiegreiner/palette-picker/blob/master/test/routes.spec.js#L82) test are pretty much identical to the next [test](https://github.com/robbiegreiner/palette-picker/blob/master/test/routes.spec.js#L126). What you really want to do is have some additional seed data so that you can have palettes that exist under a *different* project, and you can verify that only the palettes that belong to a particular project are returned from `/api/v1/projects/:id/palettes`. Otherwise these tests don't really tell me that endpoint is working accurately -- it could accidentally be returning all palettes for all projects, as that's what your first test and endpoint are doing.

* Your describe blocks [here](https://github.com/robbiegreiner/palette-picker/blob/master/test/routes.spec.js#L182) and [here](https://github.com/robbiegreiner/palette-picker/blob/master/test/routes.spec.js#L215) are identical, though they contain different types of tests. That's a sure sign of copy-pasta ;)

* Missing sad paths for POST requests that fail due to user error


## Commented Server File

**x points**: (10 possible points)

## JavaScript Style

**x points**: (30 possible points)

* Some weird spacing on this [line](https://github.com/robbiegreiner/palette-picker/blob/master/test/routes.spec.js#L38) around those parens

## Workflow

**x points**: (20 possible points)


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
