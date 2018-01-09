# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/lfinney/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-lfinney.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/lfinney/palette-picker/blob/server-commentary/server.js)

## Completion

#### Were you able to complete the base functionality?

If not, explain what is missing and why.

Yes, barely.

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/lfinney/palette-picker/blob/master/public/js/index.js#L159-#L166)

* Why were you proud of this piece of code?
This was one of the last pieces of functionality that I wrote. I was able to put it together quite quickly, and it's clean and concise.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/lfinney/palette-picker/blob/master/public/js/index.js#L17-#L37)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
Ideally, I would not like to have this much html in a js file. Initially, I tried to keep the html in the index.html file as a template and create a new copy as needed. I ran into problems with styling and appending the proper data from the database.

Now that I have a bit more experience with jQuery and better understand the server-client relationship, I think I could get my intial idea to work.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
<img width="1254" alt="palette-picker-test-suite" src="https://user-images.githubusercontent.com/22566946/33490870-b1c02574-d675-11e7-823a-99e714285e96.png">

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

As a general rule, I like matte colors and simple designs. [Color Hunt by Gal Shir](https://cdn.dribbble.com/users/729829/screenshots/3845170/galshir-colorhunt.gif) displays colors in succession using no borders. I tried to style my app without using any borders, but instead relying on the contrasting colors to "draw" the sharp lines for one's eye. ~I also experimented with adding some drop shadow, which Gal also does, but couldn't quite get it to look as I wanted. I tried attempting to use whites and grays to contrast the black palette of my overall app, but all the colors I attempted didn't look to pleasing to the eye.~ Added the drop shadow and just went with a darker black. It makes the page containers less flat.

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**45 points**: (50 possible points)

* Lock/un-lock is not working in production (assets or links to assets might have been moved around for PWAs)
* Everything else seems to be working great!

## User Interface

**16 points**: (20 possible points)

* Something on production is messing with the lock/un-lock icons when you toggle them
* Overall, pretty pleasant
* The text on the forms is a bit small on a high-resolution laptop screen

## Testing

**15 points**: (20 possible points)

* If you return the promise (`return chai(...)`), then you should not need to use the [`done()` callback function](https://github.com/lfinney/palette-picker/blob/master/test/route.spec.js#L58) in this and other tests
* [This part of your test](https://github.com/lfinney/palette-picker/blob/master/test/route.spec.js#L191-L199) can be overkill depending on the dev team you're working on. Some will want the check by making a request, and some will want to assume that unless you get any errors, the DB has done it's thing correctly. Just keep in mind not to nest too many requests or else the test can be difficult to read.
* Would want to see a sad path around a POST request where a param is missing from the body
* [This](https://github.com/lfinney/palette-picker/blob/master/test/route.spec.js#L281) should be a 404 response because the resource does not exist - the structure of the request is OK
* Overall, good happy path testing

## Commented Server File

**8 points**: (10 possible points)

* Not sure [here](https://github.com/lfinney/palette-picker/blob/server-commentary/server.js#L9) what you mean by "connects", middleware would be a good term to use - some other vague terms used in the file
* Overall, very good commented server file

## JavaScript Style

**22 points**: (30 possible points)

* You do not need an explicit `return` [here](https://github.com/lfinney/palette-picker/blob/master/server.js#L30) or in other route handlers unless, for instance, you have a response formed within an if/else conditional
* [This](https://github.com/lfinney/palette-picker/blob/master/server.js#L88-L94) is a good portion of code where you could refactor into its own function or middleware since you're doing the same thing in another POST request route handler - the only difference is the params that are expected
* [This](https://github.com/lfinney/palette-picker/blob/master/server.js#L134) response should be 404
(using [this file version](https://github.com/lfinney/palette-picker/blob/0d2503640b0c265cea104e69b778c6988673eee0/public/js/index.js) for your public JS)
* One thing to note with using `fetch` is that it will not error on 404 - in order to hit the `.catch` on a 404, you can check for `response.ok` [demonstrated in the MDN docs here](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch#Checking_that_the_fetch_was_successful)
* Make sure to use `catch()` in every [fetch call](https://github.com/lfinney/palette-picker/blob/0d2503640b0c265cea104e69b778c6988673eee0/public/js/index.js#L52) or anything promise based - technically this one is OK because it will hit a catch eventually in another function, but if someone else used the `fetchPalettes` function somewhere else, then they wouldn't have the `catch`
* Would [extract this](https://github.com/lfinney/palette-picker/blob/0d2503640b0c265cea104e69b778c6988673eee0/public/js/index.js#L20-L32) to its own function or an HTML template like you said above
* [This function](https://github.com/lfinney/palette-picker/blob/0d2503640b0c265cea104e69b778c6988673eee0/public/js/index.js#L114-L138) is getting long and has multiple responsibilities

## Workflow

**17 points**: (20 possible points)

* Good job adding `.gitignore` file early on in the project
* Want to see smaller, more atomic commits


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 123 / 150

